# LSTM stock predictors: Closing Prices vs. Fear & Greed 'FNG') Index

## Notebook 1: 1_lstm_stock_predictor_closing_prices
In this notebook we:  
* Import our initial libraries and their dependencies (ln 1).
* Set the random seed for reproducibility (ln 2).
* Load the fear and greed sentiment data for Bitcoin (ln 3).
* Load the historical closing prices for Bitcoin (ln 4). 
* Join the data into a single DataFrame (ln 5). 
* Display the first 5 lines of the new combined dataframe (ln 6). 
* Create a function that (1) accepts the column number for the features (X) and the target (y), (2) chunks the data up with a rolling window of Xt-n to predict Xt, and (3) returns a numpy array of X and y (ln 7). 
* Predict Closing Prices using a 10 day window of previous closing prices, then experiment with window sizes anywhere from 1 to 10 and see how the model performance changes (ln 8). 
* Use 70% of the data for training and the remainder for testing (ln 9). 
* Scale the data (ln 10). 
* Reshape the features for the model (ln 11). 
* Import dependencies from tensorflow (ln 12). 
* Build the LSTM model (ln 13). 
* Compile the model (ln 14). 
* Summarize the model (ln 15). 
* Train the model (ln 16). 
* Evaluate the model (ln 17). 
* Make some predictions (ln 18). 
* Recover the original prices instead of the scaled version (ln 19). 
* Create a DataFrame of Real and Predicted values (ln 20). 
* Plot the real vs predicted values as a line chart (ln 21). 

## Notebook 2: 1_lstm_stock_predictor_fng 
In this notebook we:  
* Import our initial libraries and their dependencies (ln 1).
* Set the random seed for reproducibility (ln 2). 
* Load the fear and greed sentiment data for Bitcoin (ln 3). 
* Load the historical closing prices for Bitcoin (ln 4). 
* Join the data into a single DataFrame (ln 5). 
* Display the first 5 lines of the new combined dataframe (ln 6). 
* Create a function that (1) accepts the column number for the features (X) and the target (y),(2) chunks the data up with a rolling window of Xt-n to predict Xt, and (3) returns a numpy array of X and y(ln 7). 
* Predict Closing Prices using a 10 day window of previous fng values, then experiment with window sizes anywhere from 1 to 10 and see how the model performance changes (ln 8). 
* Use 70% of the data for training and the remainder for testing (ln 9). 
* Scale the data (ln 10). 
* Reshape the features for the model (ln 11). 
* Import the relevant dependencies from tensorflow (ln 12). 
* Build the LSTM model (ln 13). 
* Compile the model (ln 14). 
* Summarize the model (ln 15). 
* Train the model (ln 16). 
* Evaluate the model (ln 17). 
* Make some predictions (ln 18). 
* Recover the original prices instead of the scaled version (ln 19). 
* Create a DataFrame of Real and Predicted values (ln 20). 
* Plot the real vs predicted values as a line chart (ln 21). 


# Concluding Questions & Answers: 
* Q: Which model has a lower loss?
* A: lstm_stock_predictor_closing_prices has a lower loss of between 1.1% and 19.1% using 10 epochs, compared to lstm_stock_predictor_fng that has a loss of between 5% and 19.5% for the same number of epochs.  

* Q: Which model tracks the actual values better over time?
* A:lstm_stock_predictor_closing_prices tracks the actual values better, given its (X_test,  y_test) evaluation score of 0.009975461289286613, compared to lstm_stock_predictor_fng's evaluation score of 0.09929212182760239. Further,  the small difference between lstm_stock_predictor_closing_prices' Real and Predicted values (between 1.8% to 5.8%) with its Real vs. Predicted Values plot shows that closing prices tracks actual values better, compared to lstm_stock_predictor_fng's Real and Predicted values difference of -44% to -45%. 

* Q: Which window size works best for the model?
* A: A window size of 10 works best for the model. 

