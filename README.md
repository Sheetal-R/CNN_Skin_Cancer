# CNN_Skin_Cancer
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

# Project Name
> Skin cancer ISIC The International Skin Imaging Collaboration


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
### Problem Statement:
- To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
- There are 2239 train and 118 test images for generating a model to detect melanoma.
- The classes of melanoma covered are as follows:
   - Actinic keratosis
   - Nevus
   - Seborrheic keratosis
   - Dermatofibroma
   - Pigmented benign keratosis
   - Vascular lesion
   - Squamous cell carcinoma
   - Basal cell carcinoma
   - Melanoma

### Solution:
- The solution was developed using google colabs.
- Google drive was used to hold images that were used for run the model and to store the Augumented samples created for enhancing model accuracy.
- Different Conv2D, MaxPooling2D, Dropout and data_augmentation were tried and used to generate model.
- Optimizer - 'adam', loss -tf.losses.SparseCategoricalCrossentropy(from_logits=True), metrics -'accuracy' was chosen for model compiling

## Conclusions
### Summary
 - Model Building & training :
    - Created a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0,1).
    - Selected 'adam' optimiser and loss function 'tf.losses.SparseCategoricalCrossentropy(from_logits=True)' for model training
    - Train the model for ~20 epochs
  - The data augmentation strategy with random zoom, rotation, flip was chosen to resolve overfitting
  - Model Building & training on the augmented data :
    - Created a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
    - Selected 'adam' optimiser and loss function 'tf.losses.SparseCategoricalCrossentropy(from_logits=True)' for model training
     - Train the model for ~20 epochs
     - The dropout helped in reducing the overfit problem along with data augumentation
  - On examining the current class distribution in the training dataset
     - Classes dermatofibroma, melanoma least number of samples
     - Classes nevus, vascular dominate the data in terms proportionate number of samples
  - Rectified class imbalances present in the training dataset with Augmentor library
  - Model Building & training on the rectified class imbalance data :
     - Created a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
     - Selected 'adam' optimiser and loss function 'tf.losses.SparseCategoricalCrossentropy(from_logits=True)' for model training
     - Train the model for ~30 epochs
     - This increased the model accuracy to nearly 80-90% which is very significant

## Technologies Used
- pathlib 
- tensorflow
- tensorflow.keras
- tensorflow.keras.models
- matplotlib.pyplot
- Augmentor
- PIL
- os, numpy, pandas
- google.colab
- glob

## Acknowledgements
This project perfored as part of the IIT-B /Upgrad EDG Program


## Contact
Created by Sheetal R
