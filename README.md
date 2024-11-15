# Neural Network Challenge 2

## Overview

This project involves building a branched neural network to predict two key outcomes for employees:

1. Attrition: Whether an employee is likely to leave the company.

2. Department: The department that best suits each employee.

The neural network is trained using preprocessed employee data and consists of shared hidden layers followed by two output branches: one for attrition (binary classification) and one for department prediction (multi-class classification).

## Table of Contents

- Technologies Used

- Dataset

- Project Workflow

- Results

- Model Improvements

- File Structure

- How to Run the Code

## Technologies Used

- Python 3.10

- TensorFlow / Keras

- Scikit-learn

- Pandas

- Numpy

## Dataset

The dataset contains employee data with features like:

- Age

- DistanceFromHome

- Education

- JobSatisfaction

- WorkLifeBalance

- YearsAtCompany
  
## Target columns:

- Attrition (Binary: Yes/No)

- Department (Multi-class: Sales, Research & Development, etc.)

##  Project Workflow

### Part 1: Preprocessing

1. Import Data:

   - Load and view the dataset.

2. Explore the Data:
   
   - Count unique values in each column.

3. Target and Feature Separation:
   
   - Create y_df for target columns (Attrition and Department).

   - Select 10 features for X_df from the dataset.

4. Data Transformation:
   
   - Split the data into training and testing sets.

   - Scale X features using StandardScaler.

   - Encode categorical target columns using OneHotEncoder.

### Part 2: Neural Network Creation

1. Input and Shared Layers:

   - Define an input layer.
     
   - Add two shared dense layers.

2. Branched Output Layers:
   
   - One branch for predicting attrition using a sigmoid activation function.

   - One branch for predicting the department using a softmax activation function.

3. Model Compilation:

   - Loss Functions:

- binary_crossentropy for attrition prediction.

- categorical_crossentropy for department prediction.

   - Metrics:
     
- Accuracy for both branches.

4. Model Training:

   - Train the model for 50 epochs with a batch size of 32.

   - Validate performance on the testing dataset.

### Part 3: Evaluation and Summary

1. Evaluate the Model:

   - Compute total loss and accuracy for both output branches.

2. Summary of Findings:

   - Discuss metrics, activation functions, and potential improvements.

## Results

### Performance Metrics:

- Department Accuracy: ~60%

- Attrition Accuracy: ~83%

These metrics demonstrate the model’s ability to predict department classifications and attrition likelihood based on the provided employee features.
