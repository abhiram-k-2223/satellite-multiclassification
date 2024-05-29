# Satellite Classification 

## Project Overview

This repository contains code to classify satellite using machine learning techniques. The project explores multiple models and evaluates their performance to determine the most accurate classifier for this dataset.

## Dataset

The dataset used for this project contains satellite images categorized into different classes. Each row represents an image with several features, and the target variable is the class to which the image belongs.

## Steps Involved

### 1. Data Loading and Exploration

- **Loading the Data:** The dataset is loaded using Pandas.
- **Initial Analysis:** We check for any duplicate entries and missing values to ensure data quality.

### 2. Data Preparation

- **Feature and Target Separation:** The features and target variable (`Class`) are separated for model training.
- **Train-Test Split:** The data is split into training and testing sets to evaluate model performance.

### 3. Model Training and Evaluation

We employ multiple machine learning models to classify the satellite images:

#### Logistic Regression

- **Model:** Multinomial Logistic Regression with the `lbfgs` solver.
- **Training:** The model is trained on the training data.
- **Evaluation:** Initial accuracy is calculated using the test set.

#### Standardization

- **Scaler:** StandardScaler is used to normalize the features for improved model performance.
- **Retraining:** Logistic Regression is retrained on the scaled data.
- **Evaluation:** The accuracy is recalculated on the scaled test set.

#### Support Vector Classifier (SVC)

- **Model:** Linear SVC with a regularization parameter `C` set to 1.
- **Training:** The model is trained on the scaled training data.
- **Evaluation:** Accuracy is calculated using the scaled test set.

#### K-Nearest Neighbors (KNN)

- **Model:** K-Nearest Neighbors Classifier.
- **Training:** The model is trained on the scaled training data.
- **Evaluation:** Accuracy is calculated using the scaled test set.

## Results

The performance of each model is evaluated based on accuracy:

- **Logistic Regression (Unscaled Data):** Achieves an initial accuracy score.
- **Logistic Regression (Scaled Data):** Accuracy improves after scaling the data.
- **Support Vector Classifier:** Provides a competitive accuracy score on scaled data.
- **K-Nearest Neighbors:** Evaluated for accuracy on scaled data.

## Conclusion

This project demonstrates the effectiveness of different machine learning models for satellite image classification. Scaling the data significantly improves the performance of the classifiers, and the comparison of models helps in selecting the best one for the task.

## How to Use

1. **Clone the Repository:** `git clone https://github.com/abhiram-k-2223/satellite-multiclassification.git`
2. **Navigate to the Directory:** `cd <satellite-multiclassification>`
4. **Run the Notebook:** Run the cod ein the notebook to train models and evaluate their performance.
