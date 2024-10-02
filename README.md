 COMP2008 ASSIGNMENT 2

 SET UP
1. Pull this repo
2. Download and extract the Data.zip from the LMS to the root directory inside Data/ . This is ignored from Git due to the large size.

 BRIEF WORKFLOW (TBD)
1. Use the root repository for group shared file (EDA, Model, etc.)
2. Make a folder with your name (eg: khang\ ) to store your personal messing with EDA, etc.

 FILES:
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

## Notes on notebooks

Khang:

Cleaning of all files, especially crawling and mapping locality to LGA for HousingPrice,
aggregating and normalizing Communities column, grouping of almagated LGA in EGM Loss,
and other cleaning mentioned in the report: <b> khang/preProcessing.ipynb</b>

Cleaned csvs are included in <b>cleanedCsv</b> folder.

All visuals for Correlation Analysis section (scatterplot, box plot, bar charts), and 
other personal EDA: <b>khang/eda.ipynb</b>

All Tree/ Community-focused Modelling: khang/model.ipynb
Linear Regression Testing (Include in Terry's script for final evaluation): <b>khang/modelNoComm.ipynb</b>

Another Scripts to produce bar chart/ bubble from pred.csv and population.csv
for future population count: <b>khang/prediction.ipynb</b>

Remaining is to test other's scripts, and models.

