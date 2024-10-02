# COMP2008 ASSIGNMENT 2

## SET UP
1. Pull this repo
2. Download and extract the Data.zip from the LMS to the root directory inside Data/ . This is ignored from Git due to the large size.

## BRIEF WORKFLOW 
1. Use the root repository for group shared file (EDA, Model, etc.)
2. Make a folder with your name (eg: khang\ ) to store your personal messing with EDA, etc.

## FILES:
1. lgaLocality: Information of locality for each LGA scraped from: https://www.vic.gov.au/know-your-council 
(LIMITATION: The website contains typo and list)

2. localityToLGA: The mapping for the Housing price locality to LGA.
Constructed by using the scraped data, then check if the locality in HousingPrices (stripped from NSEW direction) matches the listed community.
For missing community from the scraped list, manually search for it:
```
 handMapLocalityToLGA = {'aintree': 'melton', 
                       'balcombe': 'wodonga', 
                       'benalla': 'benalla', 
                       'bonniebrook': 'melton', 
                       'botanicridge': 'casey', 
                       'capelsound': 'morningtonpeninsula', 
                       'cobblebank': 'melton', 
                       'coonanshill': 'merribek', 
                       'danyo': 'mildura', 
                       'deanside': 'melton', 
                       'deepdene': 'boroondara', 
                       'eastwood': 'eastgippsland', 
                       'fiveways': 'latrobe', 
                       'fraserrise': 'melton', 
                       'glenwaverley': 'monash', 
                       'harkness': 'melton', 
                       'jolimont': 'greatershepparton', 
                       'laralake': 'greatergeelong', 
                       'lucas': 'ballarat', 
                       'manorlakes': 'wyndham', 
                       'mansfield': 'mansfield', 
                       'mckenziehill': 'mountalexander', 
                       'merindapark': 'casey', 
                       'pattersongardens': 'brimbank', 
                       'sanctuarylakes': 'wyndham', 
                       'sthelena': 'banyule', 
                       'strathtulloh': 'melton', 
                       'thornhillpark': 'melton', 
                       'weirviews': 'melton', 
                       'westall': 'greaterdandenong', 
                       'westgarth': 'nillumbik', 
                       'wimbledonheights': 'basscoast', 
                       'wintervalley': 'ballarat', 
                       'woolamaiwaters': 'basscoast'}
```

## cleanedCsv
Cleaned csvs are included in here.

## Notes on notebooks

## Khang:

### khang/preProcessing.ipynb
Cleaning of all files, especially crawling and mapping locality to LGA for HousingPrice,
aggregating and normalizing Communities column, grouping of almagated LGA in EGM Loss,
and other cleaning mentioned in the report

### khang/eda.ipynb
All visuals for Correlation Analysis section (scatterplot, box plot, bar charts), and 
other personal EDA

### khang/modelNoComm.ipynb
All Tree/ Community-focused Modelling: khang/model.ipynb
Linear Regression Testing (Include in Terry's script for final evaluation)

### khang/prediction.ipynb
Another Scripts to produce bar chart/ bubble from pred.csv and population.csv
for future population count

Remaining is to test other's scripts, and models.

## Michael folder

###  `eda_communities.ipynb`
---
Contains code for EDA on population. Graphs used in the report are labelled with the heading "Used In Report". Simply run the notebook to generate graphs and statistics are printed in the outputs.

###  `model.ipynb`
---
Contains the code for the linear regression model for population, and code to generate the population predictions for 2024. The sections in order are: preprocessing for the model, model training, predictions, null and baseline models to compare against. Simply run the notebook to generate the graph and RMSE values.

###  `model_sensitivity_[removed_feature].ipynb`
---
Each file contains a modified regression model with a feature removed for sensitivity analysis. For each model it outputs the new RMSE value.

###  `eda1.ipynb`, `eda2.ipynb`
---
These two files contain some initial EDA analysis I did on the datasets. They are less important because the results are not used in the final report.

# Terry folder

## terry/modelling.ipynb
Code for training all the models for the time series modelling. Requires preprocessed and cleaned data from `terry/eda.ipynb`.

First section preprocesses the cleaned data for model inputs. Second section performs CV on the train-validation set, then evaluates it on the test set. Last section generates forecasts.

## terry/eda.ipynb
Code for generating the complete preprocessed dataset, and performances EDA. Requires cleaned EGM and Community data from `khang/preprocessing.ipynb`.

First section cleans and joins the datasets. Second section produces time-series EDA graphs.

