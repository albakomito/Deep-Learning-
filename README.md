# Unit_14_Assignment-Questions

## 1_lstm_stock_predictor_closing_prices 
* Ln 15: output differs from starter code (10 vs. 30 output shape)- way fewer parameters. 
* Ln 16: is batch size too small? Output very different. 
* Ln 18: Only 1 prediction? 
* Ln 19: right to define y_test_scaler (not given)? 
* Ln 20: Predicted values significantly different? 

## 2_lstm_stock_predictor_fng
* Ln 15: Identical to Notebook 1 (Ln 15). 
* Ln 18: same as Notebook 1 (Ln 18). 
* Ln 20: Predicted values significantly different? 


## Concluding Questions & Answers (to confirm): 
* Q: Which model has a lower loss?
* A: lstm_stock_predictor_closing_prices has a lower loss when using 10 epochs. 

* Q: Which model tracks the actual values better over time?
* A:lstm_stock_predictor_closing_prices tracks the actual values better, given its (X_test,  y_test) evaluation score of 0.04780703783035278. 

* Q: Which window size works best for the model?
* A: 10... 
