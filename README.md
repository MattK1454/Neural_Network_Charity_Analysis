# Neural Network Charity Analysis

## Overview

The purpose of this project was to use data regarding past loans provided by the Alphabet Soup Charity organization to develop a neural network
to predict success of future loan applications. 

## Results

* Data Processing

	* Target variables 

	![target variables](https://github.com/MattK1454/Neural_Network_Charity_Analysis/blob/main/Resources/images/target_variables.png)

	The variable set for targeting in the neural network is the "IS_SUCCESSFUL" variable from the data.

	* Feature variables

	![feature variables](https://github.com/MattK1454/Neural_Network_Charity_Analysis/blob/main/Resources/images/feature_variables.png)

	The feature variables for the neural network are: "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", 
	"STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", and "ASK_AMT".
	
	* Removed variables

	![drop variables](https://github.com/MattK1454/Neural_Network_Charity_Analysis/blob/main/Resources/images/drop_variables.png)
	
	Variables dropped from the data include: "EIN" and "NAME"

* Compiling, Training, and Evaluating the Model

	* Neurons, layers, and activation functions
	
	![neural network structure](https://github.com/MattK1454/Neural_Network_Charity_Analysis/blob/main/Resources/images/nn_structure.png)
	
	For this particular model, 43 input features were selected with 2 hidden layers, the first hidden_layer has 86 neurons and the second 
	layer has 20. The two layers both use Relu activation functions for the output. The final output neuron uses the sigmoid activation function. 
	86 neurons were selected for the second layer as that is 2 neurons per input feature. The relu activation function was selected as it eliminates 
	negative values for the inputs. Sigmoid activation was used on the output as it helps to sort values into dichotomos values as determined by 
	the target value.
	
	* Target performance
	
	![network performance](https://github.com/MattK1454/Neural_Network_Charity_Analysis/blob/main/Resources/images/target_performance.png)
	
	I was not able to achieve a 75% accuracy with the steps I attempted to use for optimization. I was only able to achieve the 72.4% accuracy.
	
	* Steps to increase model performance
	
	![model adjustments](https://github.com/MattK1454/Neural_Network_Charity_Analysis/blob/main/Resources/images/opti_steps.png)
	
	Steps attempted to optimize the model:
	
		* Increase neurons in the first hidden layer to 3 neurons per input feature.
		* Double the number of neurons in the second layer.
		* Added a third hidden layer with half the neurons of the second layer.
	
## Summary

The deep learning model developed achieved approximately 73% accuracy in determining the success of loans provided by the Alphabet Soup Charity. This 
model contained 43 input features as a basis for the model development and at least 2 hidden layers of neurons for analysis. As all of my steps failed 
to improve the accuracy of the model, it may be possible to use a different model such as a Random Forest Classifier (RFC) ensemble model to achieve 
similar or better results to the neural network. With the data already scaled, the RFC can use the 43 feature variables to analyze various 
combinations of the features to allow for feature variable weights to be determined. Since the RFC can be implemented with less training time and 
the RFC model should be able work well with the limited provided data, the RFC model may be able to achieve similar or better results until more 
data can be obtained for the neural network training.

## References
1. Module 19 Challenge. (n.d.). Retrieved February 14, 2021, from https://courses.bootcampspot.com/courses/453/assignments/6732