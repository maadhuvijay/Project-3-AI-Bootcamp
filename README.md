# Project-3-AI-Bootcamp


## Dataset collection

1. Source: Lego images from Kaggle [https://www.kaggle.com/code/stpeteishii/lego-bricks-classify-torch-linear-conv2d]
2. Image selection: Each lego piece has 800 images. Total 1132 Images for 4 lego brick pieces -2357, 3001,3010,3022 [283 each] were chosen
3. Lego images used: The front and top angle of pieces were chosed. 

## Data Exploration
The lego image was printed / plotted to ensure the import was successful.


![image](https://github.com/user-attachments/assets/1668dcd7-ae98-498c-b31f-32fbc03d2bf4)


## Data Pre-processing

Below pre-processing steps were done on the lego images. 

1. Re-sizing of the images to 224 x 224 from 400 x 400.
   
   ![image](https://github.com/user-attachments/assets/2fa077f2-05a7-4a7e-8f84-407ea93a2752)


2. Edge detection and Dilation of edges were done on the images to make the edges prominent.


![image](https://github.com/user-attachments/assets/9e2cf0ac-671e-457f-b8c0-da946a331f1d)



3. The images were then added padded to re-size it into 128 x 128 within the image .
4. Normalize the image so that the pixel values are between 0 and 1.
5. The images were converted to grayscale and were added channel dimension 1 for grayscale image.

![image](https://github.com/user-attachments/assets/5b3fb759-15c2-471b-8614-299e78d1bc92)

## Training testing data split
1. The normalized images are the X data.
2. The design ID of the lego piece is the target column (y)


## Image Augmentation
The 1132 images were then augmented to add more diverse images to the dataset.

Below **random transformations** were performed.

1. Random flip (Horizonatl)
2. Random Zoom
3. Random flip (Vertical)

## Converting the y-data to numerical data
1. The y-column with Lego design id's were encoded to numerical data through **One-hot encoding**. 



# Model selection


**CNN model** was built and trained to classify these Lego images due to its capability of classifying images. 

The model was created with 3 Convulation layers, 1 flatten layer and 2 dense layers and one of them being the output layer.

![image](https://github.com/user-attachments/assets/d8e1b5bc-d1b6-45b7-8c44-094928db45b3)


## Model training

The model was trained with

1. Activation funcitons **"relu"** on the convolution layers and **"softmax"** for the output layer as this is a multi-class image classification problem.
2. The model used **"categorical cross entropy"** for the loss function and measured **"Accuracy"** as the validation metric.
3. **Early stopping** is used as a training technique used to prevent overfitting in the model.

## Model Optimization

4 models were built: 1 main model and 3 models to analyze the below optimatization techniques.

1. **L1 regularization**


  ![image](https://github.com/user-attachments/assets/ca3cf1ac-aec6-4a99-b0b2-ea6dd4b96838)
  ![image](https://github.com/user-attachments/assets/a73e5220-09ca-4283-9609-b1447dfb0aa6)


2. **L2 regularization**

   ![image](https://github.com/user-attachments/assets/a2d91fe9-8013-4d28-83c5-b4bd6521b0bd)
   ![image](https://github.com/user-attachments/assets/9eabd546-c69d-4c30-97a0-d66116c21692)


4. **Dropouts**

   The dropouts model also showed a similar results like L2 regularization technique and not more deviated results like L1 regularization

**In the final model**, it was decided 

   1. To add a dropout later after the dense layer
   2. To add L2 regularizer to the layers with higher parameters. 

## Model evaluation
## Model prediction

## Gradio - User Inferface



## Reference


   
   
   

