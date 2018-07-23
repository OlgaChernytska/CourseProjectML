# Predicting bus time to arrival at stops using GPS data only.

Throughout this project the following tasks were completed:

1) Data was transformed from data frame ’time - vehicle id - latitude - longitude’ to ’drive id - starting stop - ending stop - travel time in seconds’.

2) Transformed data was used to train a model. Linear regression was selected to be a baseline model; it results in median absolute error of 30.86 seconds on test set. Baseline model was improved by 40% based on median absolute error decrease to 21.77 seconds on test set. This was done by excluding outliers from train set, changing model to be Gradient boosting regressor and tuning its parameters using Grid search.

3) Developed working demo, that accepts bus GPS location, direction and time as inputs, and produces data frame that contains seconds to arrival and arrival time for the next 5 stops on the route.