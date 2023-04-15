##CarDekho Price Prediction with Determined.ai


##Project Objective


The objective of this project is to build a machine learning model that can predict the selling price of used cars based on various features like mileage, engine displacement, and more. We use the CarDekho dataset to train our model and the Determined.ai platform to optimize hyperparameters and train the best model possible.

##Data Sample


Here is an example row of data from the CarDekho dataset:

##Model Architecture
Our model architecture consists of an input layer, two dense layers, and an output layer. We use ReLU activation for the dense layers and linear activation for the output layer since we are performing regression. We use the mean squared error as our loss function and the Adam optimizer to minimize it.

##How to Run the Training Job
Install the Determined.ai CLI tool by following the instructions here.
Clone this repository and navigate to the project directory.
Run det deploy . to deploy the project to a Determined cluster.
Run det experiment create . to start a new experiment with the default hyperparameters.

##Best Metrics Screenshot
