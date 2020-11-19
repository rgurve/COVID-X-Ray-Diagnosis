# COVID19 X-Ray Diagnosis

#COVID19 Detection from Chest X-Ray Images using Transfer Learning
Domain             : Computer Vision, Machine Learning
Sub-Domain         : Deep Learning, Image Recognition
Techniques         : Deep Convolutional Neural Network, ImageNet, Inception
Application        : Image Recognition, Image Classification, Medical Imaging

Description
1. Detected Pneumonia from Chest X-Ray images using Custom Deep Convololutional Neural Network and by retraining pretrained model “Densenet169” with 6432 images of X-ray (800+ MB).
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

 Objective
 -Train a convolutional neural network to detect and classify diagnoses of patients.
 -Couple structured and unstructured datasets together into a multi classifier.
