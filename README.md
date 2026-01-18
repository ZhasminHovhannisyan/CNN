# CNN and ML Projects 

## Overview

This repository contains a collection of projects and implementations developed as part of Convolutional Neural Networks (CNN) course at NPUA.

## Repository Structure
The repository is organised into subdirectories, 
each containing a distinct project.

## Projects 

### [Project 1: Housing Price Prediction](House-Price-Prediction/)
- Description: A neural network regression model built with PyTorch to predict housing prices using tabular data.
Includes preprocessing, log-transform targets, early stopping, and visualizations like prediction vs. actual plots.
- IPython Notebook: [house-price-prediction-with-NN.ipynb](House-Price-Prediction/House-Price-Prediction-with-NN.ipynb)

### [Project 2: CIFAR10 Classification with ResNet18](CIFAR10-ResNet18/)
- Description: A ResNet18-based image classifier fine-tuned on the CIFAR-10 dataset with staged layer unfreezing.
Tracks accuracy, loss, confusion matrix, and per-class performance with automated checkpoints and plots.
- IPython Notebook: [CIFAR10-ResNet18.ipynb](CIFAR10-ResNet18/CIFAR10-ResNet18.ipynb)

### [Project 3: YOLO11m Object Detection on Pascal VOC](YOLOv11-Obj-Det-PascalVOC/)
- Description: Fine-tune a YOLO11m object detector on Pascal VOC 2007+2012 with custom data conversion, mixed-precision training, frozen backbone layers,
and evaluation via training curves and test-set mAP. Includes a Streamlit demo for real-time webcam inference.
- IPython Notebook: [YOLO-obj-det-PascalVOC.ipynb](YOLOv11-Obj-Det-PascalVOC/YOLOv11-obj-det-PascalVOC.ipynb)

### [Project 4: Single-Image 3D Reconstruction on Pix3D](Pix3D_reconstruction/)

- Description: A deep learning pipeline that reconstructs 3D point clouds from single RGB images using the Pix3D dataset. Utilizes a pretrained ResNet-18 encoder and a fully connected regression head to predict object geometry, optimizing Chamfer Distance for efficient, voxel-free surface representation.
- IPython Notebook: [3D_reconstruction_Pix3D.ipynb](Pix3D_reconstruction/3d_reconstruction_Pix3D.ipynb)

## Clone the repository
```
git clone https://github.com/ZhasminHovhannisyan/CNN.git
cd CNN

```
