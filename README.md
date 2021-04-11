# mask-rcnn-fine-tune-pisa
(WIP) Fine Tuning Mask R-CNN on Leaning Tower of Pisa Dataset

## Fine-Tuning Custom Dataset with Mask-RCNN via Detectron2

![Dectectron2](https://dl.fbaipublicfiles.com/detectron2/Detectron2-Logo-Horz.png?raw=True)

In the [Google Colab notebook](https://colab.research.google.com/github/mattignal/mask-rcnn-fine-tune-pisa/blob/main/fine_tune_pisa.ipynb), we will:

* Import and structure the custom dataset
* Fine-tune the Mask-RCNN model pre-trained on the COCO segmentation dataset using the train and validation sets in our custom data
* Run inference using the model on our testing set

Our custom dataset involves images of the Leaning Tower of Pisa. Can we use instance segmentation to find it?

![Tourists at Leaning Tower of Pisa](https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/Italy_Tower.jpeg?raw=True)

We can use [Hyperlabel](https://sixgill.com/platform/sense-data-annotation/) for quickly annotating images. 

Simply drag and drop around the image and Hyperlabel will take care of the rest.

![Hyperlabel Drag](https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/Hyperlabel%20Drag.png?raw=true)

![Hyperlabel Drag](https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/Hyperlabel%20Auto.png?raw=true)

After labeling about 80 images in less than a half hour, I exported the annotated dataset in COCO format. From there, I could fire up Dectron 2 and begin training the data.

<img src="https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/labeled_pisa.png?" height="100">

It only takes a few minutes for the model to produce amazing accuracy:

!['Tensorboard'](https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/Tensorboard_500iter.png?raw=True)

<img src="https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/pisa_test_labels.png" width="100" height="100">

