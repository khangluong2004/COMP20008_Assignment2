## terry/modelling.ipynb
Code for training all the models for the time series modelling. Requires preprocessed and cleaned data from `terry/eda.ipynb`.

First section preprocesses the cleaned data for model inputs. Second section performs CV on the train-validation set, then evaluates it on the test set. Last section generates forecasts.

## terry/eda.ipynb
Code for generating the complete preprocessed dataset, and performances EDA. Requires cleaned EGM and Community data from `khang/preprocessing.ipynb`.

First section cleans and joins the datasets. Second section produces time-series EDA graphs.

