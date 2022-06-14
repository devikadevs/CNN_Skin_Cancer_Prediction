# Skin Cancer Detection Using A Custom Convolutional Neural Network in TensorFlow


## Table of Contents
* Brief Problem Statement
* Data Understanding
* Project Pipeline
* Conclusions
* Technologies Used

<!-- You can include any other section that is pertinent to your problem -->

## Problem Statement
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Data Understanding
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.The data set contains the following diseases:
- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion

## Project Pipeline
- Data Reading/Data Understanding → Defining the path for train and test images 

- Dataset Creation→ Create train & validation dataset from the train directory with a batch size of 32. Resized the images to 180*180.

- Dataset visualization → Create a code to visualize one instance of all the nine classes present in the dataset 

- Model Building & training : 
  * Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1) i.e. divide by 255.0.
  * Chose an appropriate optimizer "adam" and loss function "SparseCategoricalCrossentropy" for model training
  * Train the model for ~20 epochs
  * Documented the findings after the model fit.

- Choosing an appropriate data augmentation strategy to resolve underfitting/overfitting i.e. "Data Augmentation for Minority Class"

- Handling class imbalances: Rectified class imbalances present in the training dataset with Augmentor library


## Conclusions
-Accuracy on training data has increased significantly by handling class imbalance using Augmentor library

-Not to forget the dataset was not sufficient for CNN model too. Added more data via data augmentation(increasing the number of samples) to solve overfitting, but overfitting persists.

-The problem of overfitting can be solved by add more layer,neurons or adding dropout layers.

-The Model can be further improved by tuning the hyperparameters


## Technologies Used
- TensorFlow
- Keras
- Augmentor
- Matplotlib
- Sequential CNN model


## Contact
Created by [@devikadevs] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
