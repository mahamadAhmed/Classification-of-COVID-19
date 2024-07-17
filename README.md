# Classification of COVID-19 Patients with and without Pneumonia using Chest X-ray Images
## Overview
This project focuses on classifying COVID-19 patients with and without pneumonia using chest X-ray images. The dataset is divided into two categories: COVID-19 patients without pneumonia and COVID-19 patients with pneumonia. The classification model utilizes logistic regression based on features extracted from the images.

Dataset
The dataset comprises chest X-ray images of COVID-19 patients, categorized as follows:

COVID-19 without pneumonia
COVID-19 with pneumonia
The images are split into training and testing sets, each containing sub-folders for the two categories.

## Preprocessing and Feature Extraction
Image Resizing: All images were resized to 256x256 pixels to ensure uniformity.
Grayscale Conversion and Normalization: Each image was converted to grayscale and normalized by dividing pixel values by 255, scaling them between 0 and 1.
Grid Division: Images were divided into a 3x3 grid, creating nine smaller regions or grid cells.
Centroid Coordinates: For each grid cell, centroid coordinates were computed, representing the weighted average of pixel coordinates with pixel intensities serving as weights. These coordinates were used as features for the classification model.
## Model
A logistic regression model was implemented for classification:

Sigmoid Function: Used to predict probabilities.
Optimization: Parameters optimized using gradient descent over 1000 iterations with a learning rate of 0.01.
Prediction: Model predicted the probability of each instance belonging to the positive class (COVID-19 with pneumonia) and assigned labels based on a threshold.
Results
The logistic regression model achieved an accuracy of 65.52% on the test set. The moderate accuracy can be attributed to:

The simplicity of the centroid features, which may not capture the complex patterns in the chest X-ray images.
The limitations of logistic regression in handling the nuances of medical image data.
Potential imbalance in the dataset and lack of data augmentation techniques.
## Conclusion
The logistic regression model using centroid features from chest X-ray images demonstrated moderate accuracy in classifying COVID-19 patients with and without pneumonia. While feasible, this approach requires significant improvements for better performance.
