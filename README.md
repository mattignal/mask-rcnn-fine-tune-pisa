# mask-rcnn-fine-tune-pisa
(WIP) Fine Tuning Mask R-CNN on Leaning Tower of Pisa Dataset

## Fine-Tuning Custom Dataset with Mask-RCNN via Detectron2

<img src="https://dl.fbaipublicfiles.com/detectron2/Detectron2-Logo-Horz.png?raw=True" width="700")

In the [Google Colab notebook](https://colab.research.google.com/github/mattignal/mask-rcnn-fine-tune-pisa/blob/main/fine_tune_pisa.ipynb), we will:

* Import and structure the custom dataset
* Fine-tune the Mask-RCNN model pre-trained on the COCO segmentation dataset using the train and validation sets in our custom data
* Run inference using the model on our testing set

Our custom dataset involves images of the Leaning Tower of Pisa. Can we use instance segmentation to find it?

<img src="https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/Italy_Tower.jpeg?raw=True" width="700")

We can use [Hyperlabel](https://sixgill.com/platform/sense-data-annotation/) for quickly annotating images. 

Simply drag and drop around the image and Hyperlabel will take care of the rest.

![Hyperlabel Drag](https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/Hyperlabel%20Drag.png?raw=true)

![Hyperlabel Drag](https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/Hyperlabel%20Auto.png?raw=true)

After labeling about 80 images in less than a half hour, I exported the annotated dataset in COCO format. 

From there, I could fire up Dectron 2 and begin fine-tuning the pre-trained model with the new annotated Pisa data.

<img src="https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/labeled_pisa.png?" height="500">

It only takes a few minutes for the model to produce amazing accuracy on such a small dataset:

!['Tensorboard'](https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/Tensorboard_500iter.png?raw=True)

<img src="https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/Italy_Tower_results.jpeg?raw=True" width="700")

<img src="https://github.com/mattignal/mask-rcnn-fine-tune-pisa/blob/main/pisa_test_labels.png" width="500">

