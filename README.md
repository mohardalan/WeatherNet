# Weather Image Recognition Project

This project focuses on the development and comparison of two Convolutional Neural Network (CNN) models for classifying an 11-class weather image database. The project includes the training of one model from scratch and the utilization of a pre-trained VGG19 model for transfer learning. 

## Table of Contents
1. [Introduction](#introduction)
2. [Data](#data)
3. [Models](#models)
4. [Results](#results)
5. [Conclusion](#conclusion)

## Introduction
The primary objectives of this project were to gain practical experience in training a CNN model from scratch and to explore the use of pre-trained models for classification tasks. The dataset used in this project was sourced from Kaggle and comprises 6862 images across 11 weather classes.

## Data
The dataset includes the following weather classes: dew, fog smog, frost, glaze, hail, lightning, rain, rainbow, rime, sandstorm, and snow. Data preprocessing involved partitioning the dataset into training, development, and test sets, and creating new directories for each set of data to facilitate the training process.

## Models
### First Model
- **Architecture:** Conv2D, Data Augmentation, Batch Normalization, ReLU Activation, MaxPooling2D, Skip Connection
- **Parameters:** 1900843 trainable, 928 non-trainable
- **Training:** Image size 128x128, batch size 32, 30 epochs

### Second Model
- **Architecture:** VGG19 (pre-trained), Dense layer (256 nodes), SoftMax layer (11 classes), Dropout (0.15)
- **Parameters:** 2100235 trainable, 20024384 non-trainable
- **Training:** Image size 128x128, batch size 64, 30 epochs

## Results
- **Model 1:** F1-Score of approximately 0.67
- **Model 2:** F1-Score of approximately 0.79, 15% better than Model 1
- Both models exhibited signs of overfitting, with Model 2 showing potential for improvement with additional data.

## Conclusion
This project provided valuable insights into the training of CNN models and the effectiveness of transfer learning in improving classification performance. Further improvements could be achieved through the use of additional data and advanced regularization techniques.
