# Neural Network Charity Analysis

This analysis was performed using Python 3.7.13 and Jupyter Notebooks. The necessary dependencies were imported from the sklearn, pandas, tensorflow, and os libraries.

## Overview of loan prediction risk analysis

The purpose of this analysis is to use the features in the previous funding data to determine whether new applicants will be successful if funded by Alphabet Soup.

## Results

* The target variable for this model was "IS_SUCCESSFUL."
* The features for this model were APPLICATION_TYPE, CLASSIFICATIONS, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, and ASK_AMT.
* The variables removed from this model were EIN, NAME, SPECIAL_CONSIDERATIONS, and AFFILIATION. 
* Due to the large number of features, three hidden layers were used to understand the complexity of the data. 80 Neurons were used in the first hidden layer to use as many neurons as two to three times the number of features. RELU was initially used as the activation function for both hidden layers and sigmoid was used as the output layer. To optimize, the activation function for hidden layers two and three was changed to tanh to attempt to capture more complexity in the data.
* Target model performance was not achieved.
* To attempt to increase model performance, variables that had potential to add noise and confusion to the model was removed. Multiple attempts of this had little positive affect. The model was adjusted by adding another hidden layer and adding neurons, unless the number of features was drastically reduced, in which case the number of neurons was adjusted to be lower accordingly. The activation functions were adjusted from a simple RELU to tanh in the hidden layers. 


## Summary

All attempts at optimization of the data failed to increase meaningfully increase performance or achieve target model performance. The analysis team recommends further analysis with random forest ensemble learning. Random forest enemble learning can handle large datasets and takes less time to train compared to the neural network approach. Most importantly, it has the functionality to assess the importance of features with `feature_importances_`, something that is not natively available in neural network learning. 