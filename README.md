# Project-3-AI-Bootcamp


## Dataset collection

1. Source: Lego images from Kaggle
2. Image selection: Each lego piece has 800 images. 3 Lego pieces (2400 images) were chosen for this classification project.
3. Lego images used:

## Data Exploration
Print an image to ensure the import was successful.


![image](https://github.com/user-attachments/assets/1668dcd7-ae98-498c-b31f-32fbc03d2bf4)


## Data Pre-processing

Re-size the image to be used to train the model.
Normalize the image so that the pixel values are between 0 and 1
Process the filename and map it to the image features.
Plot the image to check the image displays.

![image](https://github.com/user-attachments/assets/d25f328b-3fbe-4243-a2e1-30bba001a074)



## Image Augmentation
The dataset has 800 images for each lego piece depicting different angles and rotations. As an inital thought, I decided not to further augment the images.

## Training data
1. Choose the normalized images as X
2. The design ID of the lego piece is the target column (y)
3. Split the images into training and testing datasets

## Converting the y-data to numerical data
1. One hot encode the y-data to numerical values. 



## Model selection

CNN was chosen to train the model for this Lego image classification due to its capability of classifying images. 

## Model training


## Model Optimization

Below parameters were used to optimize the Model


## Model predictions



## Reference


   
   
   

