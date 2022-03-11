# Analyzing lidar-as-a-camera sensor 'images'

Analysis of object detectors and image segmentation models on images from lidar sensors

## Introduction

This work explores the potential of general-purpose DL perception algorithms, specifically detection and segmentation neural networks, for processing image-like outputs of advanced lidar sensors. We focus on low-resolution images with 360º field of view obtained with lidar sensors by encoding depth, reflectivity, or near-infrared light in the image pixels.

## Ouster Lidar Generated Images
### Signal Image
<div align="center">
<img src="./images/signal_images/left0000.jpg"/>
</div>
<!-- ![Ouster Lidar Signal Image Example](./images/signal_images/left0000.jpg) -->

### Near Infared Image
<div align="center">
<img src="./images/nearir_images/left0000.jpg"/>
</div>
<!-- ![Ouster Lidar Near-infrared Image Example](./images/nearir_images/left0000.jpg) -->

### Refectivity Image
<div align="center">
<img src="./images/reflect_images/left0000.jpg"/>
</div>
<!-- ![Ouster Lidar Reflectivity Image Example](./images/reflect_images/left0000.jpg) -->


## Preinstallation
The preinstalled environment can be seen in [recommended_env.yml](./recommended_env.yml). This is the recommeneded settings of conda virtual environment. It can been simplely create by the command below.
```
conda env create -f recommended_env.yml -n <your-env-name>
```

## Approaches
### Detection
#### Faster RCNN & Mask RCNN & YOLOv5
The implementation of these detection methods are through torchvision and torch hub models. 
The details can be seen in the [detection.ipynb](./detection.ipynb).

#### YOLOx

[YOLOx github link](https://github.com/Megvii-BaseDetection/YOLOX)
### Segmentation
#### PointRend & Mask RCNN
The implementation of Mask RCNN and PointRend are in the [segmentation.ipynb](./segmentation.ipynb).
For utilizing PointRend, we import the libary named [Pixellib](https://github.com/ayoolaolafenwa/PixelLib). The model for PointRend segmentation can be downloaded [here](https://github.com/ayoolaolafenwa/PixelLib/releases).

#### HRNet
For HRNet, we used the codes from google colab, here is the [link](https://colab.research.google.com/github/open-mmlab/mmsegmentation/blob/master/demo/MMSegmentation_Tutorial.ipynb#scrollTo=H8Fxg8i-wHJE ).


## Detection Examples
### Faster R-CNN
<div align="center">
<img src="./examples/faster-rcnn/faster22.png" width="1000" height="200" />
</div>

<!-- ![Faster R-CNN Detection Example](./examples/faster-rcnn/faster22.png) -->
### Mask R-CNN
<div align="center">
<img src="./examples/mask-rcnn/mask22.png" width="1000" height="200" />
</div>
<!-- ![Mask R-CNN Detection Image Example](./examples/mask-rcnn/mask22.png) -->

### YOLOv 5
<div align="center">
<img src="./examples/yolov5/image0.jpg" width="1000" height="200" />
</div>

### YOLOx
<div align="center">
<img src="./examples/yolox/new9.png" width="1000" height="200" />
</div>
<!-- ![YOLOx Detection Image Example](./examples/yolox/new9.png) -->


## Segmentation Examples
### PointRend
<div align="center">
<img src="./examples/pointrend/point_seg32.jpg" width="1000" height="200" />
</div>
<!-- ![PointRend Instance Segmentation Example](./examples/pointrend/point_seg32.jpg) -->

### HRNet
<!-- ![HRNet Semantic Segmentation Example](./examples/HRNet/seg2.png) -->
<div align="center">
<img src="./examples/HRNet/seg2.png" width="1000" height="200" />
</div>


## ACKNOWLEGEMENT
This research work is supported by the R3Swarms project funded by the Secure Systems Research Center (SSRC), Technology Innovation Institute (TII).

Please cite our [paper](https://arxiv.org/pdf/2203.04064.pdf) if the code or data in this repo helps your work:
```
@inproceedings{Xianjia2022AnalyzingGD,
  title={Analyzing General-Purpose Deep-Learning Detection and Segmentation Models with Images from a Lidar as a Camera Sensor},
  author={Yu Xianjia and Sahar Salimpour and Jorge Pe{\~n}a Queralta and Tomi Westerlund},
  year={2022}
}
```

