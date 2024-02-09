### Module 21 Challenge

# Analysis Report

## Overview 

This challenge involved deploying a binary classifier model that relies on the capabilities of deep learning and neural networks. The primary objective is to evaluate the likelihood of applicants securing funding from Alphabet Soup, a charitable foundation. The dataset, a comprehensive compilation covering details on a staggering 34,000 organisations, encompasses a diverse array of features. These include application types, affiliated industry sectors, government organisation classifications, funding use cases, income categories, requested funding amounts, and the effectiveness of fund utilisation.

The analysis begins with data preprocessing, involving tasks such as removing unnecessary columns, encoding categorical variables, and partitioning the dataset into training and testing sets. Following this, the neural network model is systematically developed, trained, and evaluated for both loss and accuracy.

The analysis does not conclude at this stage; attention is then directed towards optimisation. This phase entails fine-tuning the input data, adjusting the number of neurons and hidden layers, and exploring different activation functions. The objective is to achieve an optimal configuration for the model's peak performance in predicting funding outcomes.


## Data Prepocessing

### What variable(s) are the target(s) for your model?
The target variable is IS_SUCCESSFUL: The success or failure of a charitable donation hinges on this particular variable.

### What variable(s) are the feature(s) for your model?

APPLICATION_TYPE: Alphabet Soup application type.
AFFILIATION: Affiliated sector of the industry.
CLASSIFICATION: Government organization classification.
USE_CASE: Use case for funding.
ORGANIZATION: Organization type.
STATUS: Active status.
INCOME_AMT: Income classification.
SPECIAL_CONSIDERATIONS: Special considerations for application.
ASK_AMT: Funding amount requested.
 

### What variable(s) should be removed from the input data because they are neither targets nor features?

The EIN variable has been excluded from consideration due to its nature as a unique identifier for entries in the data. Its inclusion is deemed unhelpful for informing model training and testing.

## Compiling, Training, and Evaluating the Model

### How many neurons, layers, and activation functions did you select for your neural network model, and why?

First few optimisations I kept two hidden layers all with setting ReLU activation='relu'. The layers were, 80, 30 for each successive layer. My final optimisation has 4 layers 80,30,20,10. I include 'relu' (Rectified Linear Unit) as it introduces non-linearity, allowing the model to learn from the data more effectively. Each hidden layer can capture features at different levels of abstraction, allowing the network to learn complex pattern

### Were you able to achieve the target model performance?

Yes I managed to get an accuracy over 75% but it was mainly after I introduced back in the 'NAME' feature.

### What steps did you take in your attempts to increase model performance?

For Optimisation 1 , I changed application_types_to_replace = list(v_counts[v_counts<1000].index from <500. This increased the accuracy score to about 0.7317 from 0.7292

For Optimisation 2 , I kept application_types_to_replace = list(v_counts[v_counts<1000].index from <500. In addition changed classification_binning<1000 from <100. Then re-introduced the NAME variable with a value count <20. This increased the accuracy score to about 0.7710 which meant I achieved my target performance

<img width="1000" alt="namess" src="https://github.com/KajK0121/deep-learning-challenge/assets/140313204/b3bce9a7-347f-4097-918c-5e74d63d1c7c">

For Optimisation 3 , I kept application_types_to_replace = list(v_counts[v_counts<1000].index from <500. In addition changed classification_binning<1000 from <100. Then re-introduced the NAME variable with a value count <10. This increased the accuracy score to about 0.7763 which meant I improved my score to 78%

<img width="600" alt="ascore" src="https://github.com/KajK0121/deep-learning-challenge/assets/140313204/eac76cec-b068-4aaf-b01e-9ea5918b78d9">

## Summary 

In summary, the deep learning model was developed to predict the success of charitable donations based on various input features. The target variable, IS_SUCCESSFUL, was identified as the key variable determining the success or failure of a charitable donation.

The model achieved the target performance with an accuracy over 75%, primarily after reintroducing the 'NAME' feature in the optimisation process. The optimisation steps involved adjusting thresholds for categorical variables, binning, and reintroducing the NAME variable with different cutoff points. The final accuracy reached approximately 78%.

While the neural network model has shown satisfactory performance in predicting charitable donation success, considering ensemble learning methods like Random Forest or Gradient Boosting is recommended. Ensemble models offer robust predictive performance, handle complex relationships and feature interactions effectively, and are less prone to overfitting. Moreover, they provide valuable insights into feature importance, enhancing interpretability. Exploring ensemble methods presents an alternative approach with potential benefits in terms of accuracy, generalisation, and feature analysis.



