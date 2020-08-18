# Drowsiness Detection in Drivers using Deep Learning
This repository contains the files related to the project on frame-by-frame Drowsiness Detection in Drivers in videos using facial features. In this project, the aim is to extract frames from a video based data and develop a CNN model that aims to detect fatigue in a driver using facial features. A CNN-based architecture is developed for the same.

Complete details regarding the project can be viewed from the detailed [Project Report](https://github.com/neelabhsinha/Drowsiness-Detection-in-Drivers-using-Deep-Learning/blob/master/Project%20Report.pdf)

Dataset - [NTHU Drivers' Drowsiness Detection Dataset](http://cv.cs.nthu.edu.tw/php/callforpaper/datasets/DDD/)

## Models -

Two models are developed in this project, they are described as follows -

- **Baseline Model** - This is a standard model built and trained from scratch on the mentioned dataset to detect drowsiness. There is no concept of transfer learning involved.

<img src="/Model & Training Results/Baseline_Model.png" align="center" width="30%"/>


- **Final Model** - This model is built in such a way that initial layers are that of the VGG-16 Model, pre-trained on imagenet weights. The initial layers are frozen for training, allowing us to fine-tune the later layers for effective feature recognition. The recognized features are then fed to a dense network for classification.

<img src="/Model & Training Results/Final_Model.png" align="center" width="30%"/>

## Training -

The results of training accuracies vs. epochs are shown below. Complete details of architecture and results can be viewed from the [Model & Training Results](https://github.com/neelabhsinha/Drowsiness-Detection-in-Drivers-using-Deep-Learning/tree/master/Model%20%26%20Training%20Results) folder. Figure 1 is of Baseline Model, and Figure 2 is of Final Model.


<img src="/Model & Training Results/Baseline_Acc.png" align="center" width="40%"/>
<img src="/Model & Training Results/Final_acc.png" align="center" width="40%"/>

## Results & Conclusions - 

S. No. | Model | Accuracy |
-------|------|----------|
1 | Baseline Model | 68.6% |
2 | Final Model | 73.2 % |

- VGG16 model identifies features more effectively than the engineered baseline model because of more depth in the architecture, which allows it to identifiy both lower level and higher level features 
- Transfer learning helps us to make the training faster as the initial layers are used to identify local features only, which are same for almost all models. So, freezing the initial layers allows us to speed-up the training remarkably
- Features like dropout, regularization, etc. allows us to make the model more robust
- Ultimately, due to many such improvements done in the final model, it significantly outperforms the baseline model in terms of detection

## Steps to execute the code in this reposirory:

1. Install Anaconda Distribution and all relevant libraries

2. Get the licensed NTHU DDD Dataset

3. Open up the terminal and type -

``` cmd
$git clone https://github.com/neelabhsinha/Drowsiness-Detection-in-Drivers-using-Deep-Learning.git
$cd Drowsiness-Detection-in-Drivers-using-Deep-Learning
$jupyter notebook
```
