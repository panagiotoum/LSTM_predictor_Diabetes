# LSTM_predictor_Diabetes
Prediction of hypoglycemic and hyperglycemic episodes in people with diabetes type 1 using deep learning techniques, such as LSTM model.

## Data Preparation
Before a univariate series can be modeled, it must be prepared.

The LSTM model will learn a function that maps a sequence of past observations as input to an output observation. As such, the sequence of observations must be transformed into multiple examples from which the LSTM can learn.

Consider a given univariate sequence, We can divide the sequence into multiple input/output patterns called samples, where three time steps are used as input and one time step is used as output for the one-step prediction that is being learned.
