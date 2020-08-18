# Drowsiness Detection in Drivers using Deep Learning
This repository contains the files related to the project on frame-by-frame Drowsiness Detection in Drivers in videos using facial features. In this project, the aim is to extract frames from a video based data and develop a CNN model that aims to detect fatigue in a driver using facial features. A CNN-based architecture is developed for the same.

Complete details regarding the project can be viewed from the detailed [Project Report](/Project Report.pdf)

Dataset - [NTHU Drivers' Drowsiness Detection Dataset](http://cv.cs.nthu.edu.tw/php/callforpaper/datasets/DDD/)

## Models -

Two models are developed in this project, they are described as follows -

- **Baseline Model** - This is a standard model built and trained from scratch on the mentioned dataset to detect drowsiness. There is no concept of transfer learning involved.

<img src="/Model & Training Results/Baseline_Model.png" align="center" width="30%"/>


- **Final Model** - This model is built in such a way that initial layers are that of the VGG-16 Model, pre-trained on imagenet weights. The initial layers are frozen for training, allowing us to fine-tune the later layers for effective feature recognition. The recognized features are then fed to a dense network for classification.

<img src="/Model & Training Results/Final_Model.png" align="center" width="30%"/>

## Training -

The results of training accuracies vs. epochs are shown below. Complete details of architecture and results can be viewed from the [Model & Training Results](/Model & Training Results) folder.

For Baseline Model -
<img src="/Model & Training Results/Baseline_Acc.png" align="center" width="70%"/>
For Final Model -
<img src="/Model & Training Results/Final_acc.png" align="center" width="70%"/>

## Results - 

Model | Accuracy |
------|----------|
Baseline Model | 68.6% |
Final Model | 73.2 % |
