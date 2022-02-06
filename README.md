# LSTM_predictor_Diabetes
In our project we developed a LSTM predictor model, in order to predict the blood glucose levels in 30 patients with diabetes type I in the horizon of 15,30,60 and 120 minutes. Essentially the LSTM model we implement will 'learn' a function that will correspond to a sequence of previous observations (input) to an output observation. Therefore, the sequence of observations must be translated into multiple examples from which the LSTM can learn.

## Data Preparation
The set of virtual patients with SDT1 of the UVA Simulator of the University of Padua was used to develop and evaluate the model. We used data from 30 patients (10 adults, 10 adolescents and 10 children) for our work and simulated data for 1 week. The model entry area was determined to include glucose values recorded by a continuous glucose meter (Sensor), insulin values delivered by a continuous subcutaneous insulin pump (Injection) and the amount of carbohydrates in the meals received (CHO). Data collection was based on sampling every 5 minutes, according to the operating principles of continuous glucose meters. We normalized the data  (using matlab, as the data was in this format from the beginning) and then splitted into train and test set. The 70% of the dataset used for the training and the remaing for the test. We can divide the input sequence (essentially the Training Set) into multiple input / output patterns called Samples, where x time steps are used as input and 1 step is used as output for the prediction that LSTM learns. The split sequence function applies this function and splits a given sequence into multiple samples where each sample has a defined number of time steps and the output is a single time step. This is how we create Xtrain / Xtest and ytrain / ytest.

## LSTM Model
We developed LSTM model with 50 neurons and batch size 1, using KERAS library.
- Optimizer: Adam
- Activation function: ReLU
- Loss Function: MSE
- Epochs: 100

## Evaluation
Evaluation criteria:
- RMSE (root mean square error)
- MARD (mean absolute relative difference)

## Results
For the Prediction Horizon (PH) of 15 mean, we present the best graph with the lowest MARD.
![alt text](https://github.com/panagiotoum/LSTM_predictor_Diabetes/blob/main/Figures/ph%3D15min/virtual_adult1.png)
