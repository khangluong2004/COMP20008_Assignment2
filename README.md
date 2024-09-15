 COMP2008 ASSIGNMENT 2

 SET UP
1. Pull this repo
2. Download and extract the Data.zip from the LMS to the root directory inside Data/ . This is ignored from Git due to the large size.

 BRIEF WORKFLOW (TBD)
1. Use the root repository for group shared file (EDA, Model, etc.)
2. Make a folder with your name (eg: khang\ ) to store your personal messing with EDA, etc., to keep track of contribution? 

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