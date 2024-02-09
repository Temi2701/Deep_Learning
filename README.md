# Deep_Learning
Module 21 Challenge

## Overview
The goal of this analysis is to create a binary classifier using deep learning to predict the success of charitable donations funded by Alphabet Soup. The provided dataset contains information about over 34,000 organizations that received funding.

## Data Preprocessing

### Target and Features

Target variable: IS_SUCCESSFUL (Success or failure of a charitable donation).
Features include various columns such as APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, and others.

### Variables Removed

Excluded EIN and NAME columns as they are identification columns.

### Compiling, Training, and Evaluating the Model

Neural network model with 4 layers (80, 30, 20, 10 neurons).
ReLU activation used for hidden layers.
Achieved target performance with accuracy over 75%.
Steps taken to increase performance included adjusting categorical variable thresholds and reintroducing the NAME feature.

## Summary

### Recommendation

Considering the success of the neural network model, I recommend exploring ensemble learning methods like Random Forest or Gradient Boosting. Ensemble models can offer improved interpretability, generalization, and feature importance analysis.

### Report on Model Performance

Achieved target performance with accuracy over 75%.
Optimization involved adjusting categorical variable thresholds and reintroducing the NAME feature.
Consideration of ensemble methods for potential benefits in accuracy, generalization, and interpretability.
In conclusion, while the neural network model demonstrated satisfactory performance, exploring ensemble methods could provide an alternative approach with potential benefits in terms of interpretability, generalization, and feature importance analysis.
