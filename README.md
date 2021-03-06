# COVID19 X-Ray Diagnosis

#COVID19 Detection from Chest X-Ray Images using Transfer Learning

Domain             :| Computer Vision, Machine Learning
--------------------|----------------------------------
Sub-Domain         :| Deep Learning, Image Recognition
Techniques         :|Deep Convolutional Neural Network
Application        :|Image Recognition, Image Classification, Medical Imaging



__Introduction:__
----------
Deep learning, also known as hierarchical learning or deep structured learning, is a type of machine learning that uses a layered algorithmic architecture to analyze data. Unlike other types of machine learning, deep learning has an added advantage of being able to make decisions with significantly less human intervention. While basic machine learning requires a programmer to identify whether a conclusion is correct or not, deep learning can gauge the accuracy of its answers on its own due to the nature of its multi-layered structure. Many of the filtering and normalization tasks that would involve a lot of manual tasks while using other machine learning techniques, are taken up automatically.

The essential characteristics of deep learning make it an ideal tool for giving the much needed impetus, to the field of automated medical diagnosis. With the right expertise, it can be leveraged to overcome several limitations of conventional diagnosis done by medical practitioners, and take the dream of accurate and efficient automated disease diagnosis to the realm of reality.

Given the team's vision to make healthcare better for everyone, everywhere, and having paid attention to the trends and recent breakthroughs with deep learning, we decided to experiment with several variations of convolutional neural networks for this project. Recent work has shown that convolutional networks can be substantially deeper, more accurate, and efficient to train if they contain shorter connections between layers close to the input and output. We embraced this observation, and leveraged the power of the Dense Convolutional Network (DenseNet), which connects each layer to every other layer in a feed-forward fashion. Whereas traditional convolutional networks with L layers have L connections - one between each layer and its subsequent layer - our network had L(L+1)/2 direct connections. We also experimented with other architectures, including residual networks, and used our model variations as controls to validate each other.



__Description__
----------
1. Detected Covid-19 from Chest X-Ray images using Custom Deep Convololutional Neural Network and by retraining pretrained model “Densenet169” with 6432 images of X-ray (800+ MB).
2. For retraining removed output layers, freezed first few layers and fine-tuned model for three new label classes (Covid-19,Pneumonia and Normal).
3. With Custom Deep Convololutional Neural Network attained testing accuracy 97.95 and loss 0.0579 .


## Table of Contents
1. [Objective](#objective)
2. [Dataset](#dataset)
3. [Exploratory Data Analysis](#exploratory-data-analysis)
4. [Pipeline](#pipeline)
5. [Preprocessing](#preprocessing)
6. [Model (Structured Data)](#model-structured-data)
7. [Model (Convolutional Neural Network)](#model-convolutional-neural-network)
8. [Explanations](#explanations)
9. [References](#references)

## __Objective__
----------
 
 -Train a convolutional neural network to detect and classify diagnoses of patients.
 
 -Couple structured and unstructured datasets together into a multi classifier.
 
 
## __Dataset__ 
-----------

Dataset has been taken from various sources, but mostly from github

https://data.mendeley.com/datasets/rscbjbr9sj/2

https://github.com/ieee8023/covid-chestxray-dataset

https://github.com/agchung/Figure1-COVID-chestxray-dataset








Total images :| 6432 images belonging to 3 classes.
--------------|--------------------------------
Training images: | 5144 images belonging to 3 classes.
Test images :| 1288 images belonging to 3 classes.

## Explatory Data Analysis
--------

Data was analysed by reading the images of normal,pneumonia and covid X-rays

## Pipeline

Two pipelines were created for each dataset. Each script is labeled as either "Structured" or "CNN", which indicates which data pipeline the script is part of.

Description|	Script	|Model
-----------|--------|------
EDA	|eda.py	|Structured
Resize Images|	resize_images.py	|CNN
Reconcile Labels	|reconcile_labels.py|CNN
Convert Images to Arrays	|image_to_array.py	|CNN
CNN Model	|cnn.py	|CNN
Structured Data Model	|model.py	|Structured


## Preprocessing

Image data generator was used to augment images by using components like shift,height,shear and zoom to increase accuracy.
The generator also converts  single channel X-ray images (gray-scale) to a three-channel format by repeating the values in the image across all channels. We will want this because the pre-trained model that we'll use requires three-channel inputs.
 

## Model (Convolutional Neural Network)
The CNN was trained using Keras, with the TensorFlow backend.

The model is similar to the Densenet169 architecture.


Model Parameters

Machine Learning Library:| Keras and Tensorflow
-------------------------|---------------------
Base Model              :| Densenet169 && Custom Deep Convolutional Neural Network
Optimizers              :| Adam
Loss Function           :| binary_crossentropy

For Custom Deep Convolutional Neural Network :

Training Parameters

Batch Size              : |256 on training set, 50 on test set
--------------------------|-------------------------------
Number of Epochs        :| 30
Training Time           :| 36 Hours

Output (Prediction/ Recognition / Classification Metrics)

Testing

Accuracy (F-1) Score    :| 97.95%
-------------------------|---------
Loss                    :| 0.0579

ACCURACY
__________
![alt tag](https://github.com/rgurve/COVID-X-Ray-Diagnosis/blob/main/Images/Accuracy.png)

LOSS
__________
![alt tag](https://github.com/rgurve/COVID-X-Ray-Diagnosis/blob/main/Images/Loss.png)

Precision               : 88.37%                    

Recall (Pneumonia)      : 95.48% (For positive class)

[[  6   0   0]
 [  0  85   9]
 [110 232 846]]
 
 Sample Output:
 -------------
![alt tag](https://github.com/rgurve/COVID-X-Ray-Diagnosis/blob/main/Images/Prediction.png)
 
 Tech Stack
 ---------
 
 ![alt tag](https://github.com/gregwchase/nih-chest-xray/raw/master/data/tech_stack.jpg)
 
 
