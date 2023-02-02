# Machine learning - Real or fake face recognition
The purpose of the project is to implement a system for classifying images of faces into two categories:
* Pictures of real faces
* Pictures of fake faces (in the sense that the picture was created by a computer)


## Installation

This project was written in Python and developed in Jupyter. 
To run this project in Jupyter, you will need anaconda3 installed on your machine. 

Python folders - 

pip install opencv-python

* import cv2
* import glob
* import pandas as pd
* import numpy as np
* from matplotlib import pyplot as plt
* import matplotlib.image as mpimg
* import math
* from scipy.special import expit
* import os
* import matplotlib as mpl
* import itertools

Necessary dependencies for the project - 
In the folder I uploaded there are 1000 training images that are in TrainData. The images are divided into 2 directories, where there is a "real" directory that contains images of real faces and a "fake" directory that contains images of fake faces.
realPath = glob.glob("C:\\Users\\taliy\\Videos\\trainData\\real\\*.jpg")
fakePath = glob.glob("C:\\Users\\taliy\\Videos\\trainData\\fake\\*.jpg")


## Usage - Steps
 % First part - feature extraction for a classification algorithm %
1. convert the image from a color image to a grayscale image. The conversion is carried out by calculating the average of red, green and blue values in each pixel.
2. we will create a two-dimensional array with composite values.
3. centering the image by DFT to obtain a centered two-dimensional array.
4. finding the azimuthal average of the magnitude along the radii, which will help us find the spectral characteristics for each image.


% Part two - logistic regression classifier training %
1. Python implementation of the gradient descent algorithm for a logistic regression type classifier
2. Loading the data consisting of the image representations calculated by the spectral characteristics of each image and preparing it for training that is classified by labeling each of the images as real or fake
3. Training the classifier of the logistic regression type in order to check its correctness, by inserting pre-known values of real or fake
4. Examining the algorithm after the training phase - we will now implement the algorithm on images whose identity is unknown and are not available to us during the training phase. The results of the classification will be exported to a file which will update next to the name of the image whether it is real or fake.

## Identifying real images versus the behavior of fake images
<img width="341" alt="image" src="https://user-images.githubusercontent.com/87084078/216314838-fb7b7de8-7397-418d-ba75-524246a72a47.png">

For the purpose of illustration, 2 photos that cannot be distinguished who is the real one and who is not.
The fake images were created by Google -
1. real - 
<img width="397" alt="image" src="https://user-images.githubusercontent.com/87084078/216315526-410f3ca8-ffee-48cb-9684-7a1c9f36ab53.png">


2. fake - 
<img width="394" alt="image" src="https://user-images.githubusercontent.com/87084078/216315641-6c864747-112e-464d-91fd-6b5c66424ae1.png">


