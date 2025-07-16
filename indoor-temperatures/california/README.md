# Reuters prison and heat reporting data

During the process of reporting on a story that highlights the impacts of heat on the prison population, To better understand the state of heat in prisons, Reuters reach collected data on the presence of HVAC system, building age information, and internal temperature records. 

**Folder Descriptions**
- `hvac`: Includes HVAC data for state facilities from public information requests. Each state folder contains the response from the respective department of corrections. 
- `indoor-temperatures`: Contains indoor temperature log data collected from various facilities. 

## Data collection

In January 2024, Reuters began summiting public information requests to all state and federal prisons. X number of states responded.

The Bureau of Prisons, which oversees all 122 federal prisons, did not respond to Reuters’ request seeking information on how many facilities have air conditioning as of the time of publication.

Responses came in the form of emails, spreadsheets, and pdfs. 


## Data aggregation and fields

A single spreadsheet was created with the aggregated data. The 

The data is tagged with the fields of 

**facility_id**
    - The facility_id comes from the [Department of Homeland Security](https://hifld-geoplatform.hub.arcgis.com/datasets/geoplatform::prison-boundaries-1/about) (DHS) Homeland Infrastructure Foundation-Level Data (HIFLD), hosted on [this website](https://hifld-geoplatform.hub.arcgis.com/datasets/985a1fa88cac4eef94ad242a7d181a05_0/explore?location=2.785190%2C-10.417157%2C0.66). This dataset includes the geographic boundaries and attributes of "secure detention facilities" (in American states and territories) which includes prisons, jails, detention centers, re-entry facilities, jails, juvenile detention centers and more. 

    If a facility_id does not exist, it may be because the facility is new and opened since the time of the last update by the DHS. In other instances, a facility is colloquially described as a prison but may officially be categorized in another way, making it unavailable in the DHS database. 

**prison_name**
    - The name of the prison

**state**
    - The state in which the prison resides

**address**
    - The address of the prison

**ac_status**
    - The address of the prison

    Anything that is given NA means that prison did not have a corresponding document. 






- Full: All housing units have air conditioning
- Partial: As least one of the prison's housing units has air conditioning
- None: None of the housing units at a prison has air conditioning. 
- NA: Tk Tk 


## Notes

Some discrepencies may have occured since we have collected the data. A prison could have implemented air conditioning in its prison after we received the records. 
