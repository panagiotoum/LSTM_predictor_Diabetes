# LSTM_predictor_Diabetes
In our project we developed a LSTM predictor model, in order to predict the blood glucose levels in 30 patients with diabetes type I in the horizon of 15,30,60 and 120 minutes.

## Data Preparation
The set of virtual patients with SDT1 of the UVA Simulator of the University of Padua was used to develop and evaluate the model. We used data from 30 patients (10 adults, 10 adolescents and 10 children) for our work and simulated data for 1 week. The model entry area was determined to include glucose values recorded by a continuous glucose meter (Sensor), insulin values delivered by a continuous subcutaneous insulin pump (Injection) and the amount of carbohydrates in the meals received (CHO). Data collection was based on sampling every 5 minutes, according to the operating principles of continuous glucose meters. We normalized the data and then splitted into train and test set. The 70% of the dataset used for the training and the remaing for the test.
