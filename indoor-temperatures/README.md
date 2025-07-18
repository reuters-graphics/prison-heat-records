## Folder structure

Each state folder contains:
* an R script that cleans the data
* an `original/` folder that contains original data as provided by the city. 
* an `intermediate/` folder - if we did any manual data cleaning. This folder contains data after the manual data cleaning step (e.g. an `xlsx` sheet into which data from a pdf was copied).
* a `final/` folder that contains data output of the cleaning script, with columns described by the data dictionary below.



## Data dictionary

Variable name | Definition
------------- | ----------
incident_date | Date on which incident took place
incident_year | Pulled from filed_year
filed_date | Date claim or lawsuit was filed
filed_year | Pulled from filed_date
closed_date | Date at which settlement was reached OR paid (depending on what was provided)
calendar_year | Pulled from settlement date or closed_date
city | City name