**Deep Learning Assignment 01**

This repository contains the implementation and analysis of facial expression recognition and affect estimation using deep learning models.

**Project Overview**

Two CNN backbones were explored:

VGG16 (baseline, ~138M parameters)

ResNet50 (deeper network, ~25M parameters with skip connections)

Both models were trained using ImageNet pre-trained weights and fine-tuned for classification and regression tasks.

**Training Setup**

Batch size: 32

Optimizer: Adam (lr = 0.001)

Scheduler: StepLR (learning rate decay)

Epochs: 20

Loss Functions:

Cross-Entropy (classification)

MSE (affect estimation)

Data Augmentation: Horizontal flips, rotations, affine transforms, color jitter

 Results Summary

Expression Recognition (Classification):

VGG16: Validation Accuracy 48.75%

ResNet50: Validation Accuracy 46.50%

Both models showed strong overfitting despite high training accuracy (>85%).

Affect Estimation (Regression):

VGG16: Best CCC = 0.4856

ResNet50: Best CCC = 0.4895

ResNet50 performed slightly better, making it more reliable for continuous affect prediction.

**Key Insights**

Validation performance highlights the overfitting challenge.

Transfer learning improved training efficiency and generalization.

CCC (Concordance Correlation Coefficient) proved to be the most robust metric for real-world deployment.

**Author**

Omer Hafeez
Roll No: 22i-1859
Course: CS-452 – Deep Learning
Section: A
