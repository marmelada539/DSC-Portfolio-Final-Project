# DSC-Portfolio-Final-Project
My final project for data science portfolio.

CREDITS/SOURCES

CNN: Obtained public domain images from iNaturalist & Pixabay.

Regression, classification, & ROC/AUC: Used Sourav Banerjee's Animal Information Dataset from Kaggle.

POINTS

(2) Image processing: CNN image classification model of various wildcats of 4 species

(0.5) Linear model: linear regression model predicting animal height

(0.5) Logistic regression: logistic regression model classifying animals into small vs large

(1) ROC/AUC: accuracy metrics for classification model


INTRODUCTION

Wildlife conservation efforts and data science go hand in hand, as the latter is used ubiquitously in efforts to uphold the former. Having a solid understanding of zoology is essential to analyzing ecological data, which is why I bolstered the convolutional neural network wildcat image classification model with an animal dataset model that I used to study animal size. Understanding characteristics of & aiding in efforts to protect wild animals is a useful ecological and computational skillset to have as an intersection of data science and biological/environmental science.

PROCESSES

Using TensorFlow and Keras, I crafed my CNN image classification model, using data augmentation to artifically inflate the otherwise small sample size of training data images. I ran 10 epochs of the CNN model, which resulted in minor model improvement by about 20% (model accuracy grew from ~0.2 to ~0.4). I then imported, explored, and cleaned the Kaggle animal dataset, creating a function to convert object data types to numerical data values where appropriate for quantitative variables. For instance, some of the animal weight values would be input as a string containining the smaller integer and a larger integer with a hyphen in between to indicate the animal weight range, which I ensured to convert to a float value in the data cleaning function by taking the mean value between the two (so if it was "100-200," the function would average those two values together for a new value of 150, and so on). Then, I split, scaled, and trained my data, crafting a linear regression model to predict animal height, a logistic regression model with a corresponding confusion matrix, and a ROC/AUC graph.


RESULTS

Regarding accuracy metrics, pretty much every single model was really weak and in poor performance, which is a shame, as it was likely due to the small sample sizes of both the wildcat image batches as well as the limited availability of numerical, non-NaN values from the dataset from Kaggle. After 10 epochs, the CNN was low in accuracy albeit improved to say the least. The linear regression's R squared was negative, indicating poor performance; the logistic regression's confusion matrix only possessed true positives and true negatives, indicating that neither Type I nor Type II errors were made; and the AUC was an uncannily perfect 1.0 or 100%, indicating that there may be some overfitting issues.
