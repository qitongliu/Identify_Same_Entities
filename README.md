# entity-resolution
There are two datasets that describe the same entities, and I want to identify which entity in one dataset is the same as an entity in the other dataset. The datasets were provided by Foursquare and Locu, and contain descriptive information about various venues such as venue names and phone numbers.

Train files:  
locu_train.json   foursquare_train.json   matches_train.csv  
The json files contain a json-encoded list of venue attribute dictionaries. The csv file contains two columns, locu_id and foursquare_id, which reference the venue id fields that match in each dataset.  

Test files:  
locu_test.json foursquare_test.json  

Result:  
matches_test.csv, a mapping that looks like matches_train.csv but with mappings for the new test listings.  

My approach:  
•	Processed data to align the schemas and formats of the two datasets and fill missing values  
•	Created features for the random forest model and tuned parameters with cross-validation  
•	Designed matching algorithms based on the class probabilities predicted by random forest model   
