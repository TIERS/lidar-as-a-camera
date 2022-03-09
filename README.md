# Analyzing lidar-as-a-camera sensor 'images'

Analysis of object detectors and image segmentation models on images from lidar sensors

## Introduction

This work explores the potential of general-purpose DL perception algorithms, specifically detection and segmentation neural networks, for processing image-like outputs of advanced lidar sensors. We focus on low-resolution images with 360º field of view obtained with lidar sensors by encoding depth, reflectivity, or near-infrared light in the image pixels.

## Ouster Lidar Generated Images

![Ouster Lidar Signal Image Example](./images/signal_images/left0000.jpg)

![Ouster Lidar Near-infrared Image Example](./images/nearir_images/left0000.jpg)

![Ouster Lidar Reflectivity Image Example](./images/reflect_images/left0000.jpg)

## Approaches
### Detection
#### YOLOx

[YOLOx github link](https://github.com/Megvii-BaseDetection/YOLOX)
### Segmentation

## Detection Examples
### Faster R-CNN
![Faster R-CNN Detection Example](./examples/faster-rcnn/faster22.png)
### Mask R-CNN
![Mask R-CNN Detection Image Example](./examples/mask-rcnn/mask22.png)
### YOLOv 5
![YOLOv 5 Detection Image Example](./examples/yolov5/image0.jpg)
### YOLOx
![YOLOx Detection Image Example](./examples/yolox/new9.png)


## Segmentation Examples
### PointRend
![PointRend Instance Segmentation Example](./examples/pointrend/point_seg32.jpg)
### HRNet
![HRNet Semantic Segmentation Example](./examples/HRNet/seg2.png)
