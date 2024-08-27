# deep-learning-challenge

# Analysis Report

### Analysis Overview:

Alphabet Soup, a nonprofit foundation, seeks a tool to help select funding applicants with the highest likelihood of success. The goal is to develop a neural network model that can act as a binary classifier to predict the success of applicants funded by Alphabet Soup. The model will be built using data from over 34,000 previously funded organizations.

### Data Preprocessing:

The target variable for the model is IS_SUCCESSFUL:

0 indicates unsuccessful use of funding.
1 indicates successful use of funding.
The model's features include:

APPLICATION_TYPE — Type of application submitted to Alphabet Soup
FFILIATION — Industry sector affiliation
CLASSIFICATION — Classification of government organization
USE_CASE — Purpose of the funding
ORGANIZATION — Type of organization
STATUS — Current status of the organization
INCOME_AMT — Income level classification
SPECIAL_CONSIDERATIONS — Special factors considered in the application
ASK_AMT — Amount of funding requested
Identification columns EIN and NAME will be excluded from the dataset before modeling.

### Model Compilation, Training, and Evaluation:

The initial model had three layers:

First layer: 80 neurons
Second layer: 30 neurons
Output layer: 1 neuron
It used 100 epochs, with the sigmoid activation function in the output layer and the ReLU function in the hidden layers. The initial model achieved an accuracy of 73.07%.

The target accuracy was set at 75%.

To improve performance, the following modifications were made:

Increased the number of neurons and hidden layers.
Extended the training period to 150 epochs.
Converted numeric data types to binary.
Removed data deemed less relevant.
The first optimization attempt involved:

Adding 8 layers
Increasing the first layer to 129 neurons (three times the number of features)
Training for 150 epochs
This model achieved an accuracy of 72.9%.

Since increasing complexity led to a lower accuracy, the second optimization attempted:

Simplifying the ASK_AMT feature by converting it to binary values (whether it was $5000 or over $5000) instead of using unique values
This adjustment resulted in an accuracy of 72.48%.

For the third optimization:

Retained the initial model but removed the SPECIAL_CONSIDERATIONS column, as it seemed to have minimal impact
This model achieved an accuracy of 73.71%, marking the best improvement over the initial model.

## Summary:

Despite the optimization efforts, the target accuracy of 75% was not reached.

Other supervised learning methods, such as logistic regression or random forest, might be explored as alternatives to the neural network approach to potentially achieve the desired accuracy of 75%.

# Resources
***************
I used in-class activities, stackoverflow, and Xper