# Charity Success Analysis Using Keras
## Overview
This script creates and attempts to optimize a neural net model to predict whether a record with certain properties will be classified as "successful" or not. These records describe applicants for loans, with notable descriptors including the type of application submitted and amount of income earned by the applicant.

## Results
### Data Preprocessing
* What variables are considered the target for the model?
	* The target of this model was the IS_SUCCESSFUL column, which contains either a 1 or a 0 indicating whether the recipient was considered successful.
* What variable are the features for the model?
	* Use case, organization type, income amount classification, and "ask amount" are among the features that were used to predict the target outcome.
* What variables can be removed from input data?
	* Some variables we can remove outright, including "status" which doesn't describe the applicant themselves whatsoever. EIN and Name are also extraneous identifiers, which should not have any impact on the success of the recipient, so we can remove those as well.

### Compiling, Training, Evaluating the Model
* How many neurons, layers, and activation functions were selected?
	* For the most successful model, two layers were used with 8 and 5 neurons respectively. Testing was done to compare the sigmoid and tanh activation functions, but there was no clear winner that arose from those tests.
* Did the model break the 75% threshhold?
	* None of the models were more than 75% accurate.
* What steps were taken to attempt to increase performance?
	* Noisy variables were removed from the features, additional neurons were added to hidden layers, additional hidden layers were added, the activation function of output layers was changed, the amount of epochs was increased. None of these were enough to improve the model significantly.

## Summary
Although the model was not improved above 75% accuracy, the original model was 73% accurate and only ran for 100 epochs, which is relatively efficient. Future attempts to optimize this model should probably begin with a better understanding of each of the features, as pruning from the dataset may be the most direct way to improve this model.
