# Reuters prison and heat reporting data

Through public records requests, Reuters conducted an analysis of HVAC and indoor temperature log data to better understand how heat affects U.S. prisons.

During the process of reporting on a story highlighting the impacts of rising temperatures on the U.S. prison population, Reuters set out to answer: How many prisons provide cooling for inmates? How hot does it get inside prisons?

To find out, Reuters filed public records requests to every state and federal corrections department in the country asking for data on the presence of air conditioning systems in housing units and copies of indoor temperature logs. 

The absence of air conditioning in prisons can create dangerously high temperatures, potentially causing severe health issues, and in extreme cases, death. 

## Data collection

In February 2024, Reuters submitted public records requests, asking for a spreadsheet or electronic record indicating the presence of air conditioning in housing units in each adult prison. 35 states responded, with 29 states providing records.

The Bureau of Prisons, which oversees all 122 federal prisons, did not respond to Reuters’ request seeking information on how many facilities have air conditioning as of the time of publication.

In December 2024, Reuters submitted an additional round of public records requests, seeking spreadsheets or electronic records on the daily internal temperature readings for each housing area in every adult prison, covering the period from December 1, 2023, to December 1, 2024. Based on interviews with incarcerated individuals, the presence of air conditioning alone did not guarantee relief and adequately comfortable temperatures inside. Reuters identified 16 states across the country that were either in heat-prone areas or provided limited air conditioning. The federal Bureau of Prisons was not included in this request.

Responses to these requests came in the form of emails, spreadsheets and pdfs. 


## Air conditioning records 
Reuters created a single standardized spreadsheet with the responses on the presence of air conditioning in housing units.

Each prison was assigned a unique id (facility_id in the data), which matches the Department of Homeland Security’s (DHS) Prison Boundaries Database. The DHS dataset includes the geographic boundaries and attributes of prisons, jails, detention centers, re-entry facilities, jails and juvenile detention centers. 

If a facility_id is marked at NA in our spreadsheet, it may be because the facility is new and opened since the time of the last update by the DHS. In other instances, a facility may officially be categorized in another way, making it unavailable in the DHS database. 

To categorize air conditioning status, Reuters created two additional fields: ac_status and ac_status_details. 

For ac_status, a prison was marked as: 
Yes: At least one housing unit has air conditioning. This includes both mechanical air conditioning and evaporative cooling systems, commonly known as swamp coolers.
No: No housing units have air conditioning

The field ac_status_details provides additional information:
Full: All housing units have air conditioning
Partial: At least one housing unit has air conditioning
None: No housing units have air conditioning
NA: No document was available to determine AC status 













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
