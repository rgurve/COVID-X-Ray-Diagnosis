# COVID19 X-Ray Diagnosis

#COVID19 Detection from Chest X-Ray Images using Transfer Learning

Domain             : Computer Vision, Machine Learning

Sub-Domain         : Deep Learning, Image Recognition

Techniques         : Deep Convolutional Neural Network, ImageNet, Inception

Application        : Image Recognition, Image Classification, Medical Imaging

Introduction:

Deep learning, also known as hierarchical learning or deep structured learning, is a type of machine learning that uses a layered algorithmic architecture to analyze data. Unlike other types of machine learning, deep learning has an added advantage of being able to make decisions with significantly less human intervention. While basic machine learning requires a programmer to identify whether a conclusion is correct or not, deep learning can gauge the accuracy of its answers on its own due to the nature of its multi-layered structure. The emergence of modern frameworks like PyTorch, has also made preprocessing of data more convenient. Many of the filtering and normalization tasks that would involve a lot of manual tasks while using other machine learning techniques, are taken up automatically.

The essential characteristics of deep learning make it an ideal tool for giving the much needed impetus, to the field of automated medical diagnosis. With the right expertise, it can be leveraged to overcome several limitations of conventional diagnosis done by medical practitioners, and take the dream of accurate and efficient automated disease diagnosis to the realm of reality.

Given the team's vision to make healthcare better for everyone, everywhere, and having paid attention to the trends and recent breakthroughs with deep learning, we decided to experiment with several variations of convolutional neural networks for this project. Recent work has shown that convolutional networks can be substantially deeper, more accurate, and efficient to train if they contain shorter connections between layers close to the input and output. We embraced this observation, and leveraged the power of the Dense Convolutional Network (DenseNet), which connects each layer to every other layer in a feed-forward fashion. Whereas traditional convolutional networks with L layers have L connections - one between each layer and its subsequent layer - our network had L(L+1)/2 direct connections. We also experimented with other architectures, including residual networks, and used our model variations as controls to validate each other.



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

 1. Objective
 
 -Train a convolutional neural network to detect and classify diagnoses of patients.
 
 -Couple structured and unstructured datasets together into a multi classifier.
 
	2. 
