CarDekho Price Prediction with Determined.ai


Project Objective


The objective of this project is to build a machine learning model that can predict the selling price of used cars based on various features like mileage, engine displacement, and more. We use the CarDekho dataset to train our model and the Determined.ai platform to optimize hyperparameters and train the best model possible.

Data Sample


Here is an example row of data from the CarDekho dataset:

Sure! Here is an example of what the data sample table could look like:

Selling_Price	Present_Price	Kms_Driven	Fuel_Type_Diesel	Fuel_Type_Petrol	Transmission_Automatic	Transmission_Manual	Owner	Age	Mileage	Engine
0.45	            0.51      	67,000        	0               	1	                  1	                    0             	0	    9  0.11	   -0.10


Model Architecture


Our model architecture consists of an input layer, two dense layers, and an output layer. We use ReLU activation for the dense layers and linear activation for the output layer since we are performing regression. We use the mean squared error as our loss function and the Adam optimizer to minimize it.

How to Run the Training Job


Install the Determined.ai CLI tool by following the instructions here.
Clone this repository and navigate to the project directory.
Run det deploy . to deploy the project to a Determined cluster.
Run det experiment create . to start a new experiment with the default hyperparameters.

Best Metrics Screenshot
   
   
   https://i.imgur.com/Ul7ZrSc.png
   
   
Evaluation Metrics


Our model is evaluated based on the root mean squared error (RMSE) between the predicted selling price and the actual selling price. Lower RMSE values indicate better performance.

Evaluation Results


After training and evaluating multiple models with different hyperparameters, we were able to achieve an RMSE of 1.56 on the test set. This indicates that our model is able to predict the selling price of used cars with reasonable accuracy.

How to Reproduce the Evaluation Results


Follow steps 1-3 from the "How to Run the Training Job" section above.
Run det experiment create . -f experiment_config.yaml to start a new experiment with the hyperparameters and configuration specified in experiment_config.yaml.
Wait for the experiment to complete.
Run det trial list [experiment_id] to get a list of trials from the completed experiment.
Run det trial logs [trial_id] to view the logs for a specific trial and find the RMSE value on the test set.
