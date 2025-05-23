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
- Description: Fine-tune a YOLO11m object detector on Pascal VOC 2007+2012 with custom data conversion,
advanced augmentations, mixed-precision training, frozen backbone layers,
and evaluation via training curves and test-set mAP. Includes a Streamlit demo for real-time webcam inference.
- IPython Notebook: [YOLO-obj-det-PascalVOC.ipynb](YOLOv11-Obj-Det-PascalVOC/inference/YOLO-obj-det-PascalVOC.ipynb)


## Clone the repository
git clone https://github.com/ZhasminHovhannisyan/CNN.git
cd CNN/YOLOv11-Obj-Det-PascalVOC
