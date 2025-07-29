# Reuters prison and heat reporting data

This repo contains data associated with [Scorching Cells](https://www.reuters.com/graphics/USA-TEMPERATURE/PRISONS/jnpwbejwlvw/), where Reuters analyzed air conditioning and indoor temperature log data, obtained through public records requests, to better understand how heat affects U.S. prisons.

During the process of reporting on a story highlighting the impacts of rising temperatures on the U.S. prison population, Reuters set out to answer: How many prisons provide cooling for inmates? How hot does it get inside prisons?

Reuters filed public records requests to every state and federal corrections department in the U.S. asking for data on the presence of air conditioning systems in housing units and copies of indoor temperature logs. 

## Data collection

In February 2024, Reuters submitted public records requests, asking for a spreadsheet or electronic record indicating the presence of air conditioning in housing units in each adult prison. 35 states responded, with 29 states providing records and six states either denying our request or responding they did not possess or maintain records. 

The Bureau of Prisons, which oversees all 122 federal prisons, did not respond to Reuters’ request seeking information on how many facilities have air conditioning as of the time of publication.

In December 2024, Reuters submitted an additional round of public records requests, seeking spreadsheets or electronic records on the daily internal temperature readings for each housing area in every adult prison, covering the period from December 1, 2023, to December 1, 2024. Based on interviews with incarcerated individuals, the presence of air conditioning alone did not guarantee relief and adequately comfortable temperatures inside. Reuters identified 16 states across the country that were either in heat-prone areas or provided limited air conditioning. The federal Bureau of Prisons was not included in this request.

Responses to these requests came in the form of emails, spreadsheets and pdfs. 

## Air conditioning records 
The [air-conditioning](https://github.com/reuters-graphics/graphics_2025-prison-hvac-records/tree/main/air-conditioning) folder contains a single standardized spreadsheet with the responses on the presence of air conditioning in housing units. Each state folder contains the response from the respective department of corrections.

Each prison was assigned a unique id (<code>facility_id</code>in the data), which matches the Department of Homeland Security’s (DHS) [Prison Boundaries Database](https://hifld-geoplatform.hub.arcgis.com/datasets/geoplatform::prison-boundaries-1/about). The DHS dataset includes the geographic boundaries and attributes of prisons, jails, detention centers, re-entry facilities and juvenile detention centers. 

If a <code>facility_id</code> is marked as NA in our spreadsheet, it may be because the facility is new and opened since the time of the last update by the DHS. In other instances, a facility may officially be categorized in another way, making it unavailable in the DHS database. 

To categorize air conditioning status, Reuters created two additional fields: <code>ac_status</code> and <code>ac_status_details</code>. 

For <code>ac_status</code>, a prison was marked as: 
- <code>YES</code>: At least one housing unit has air conditioning. This includes both mechanical air conditioning and evaporative cooling systems, commonly known as swamp coolers.
- <code>NO</code>: No housing units have air conditioning
- <code>NA</code>: No document was available to determine AC status 

The field <code>ac_status_details</code> provides additional information:
- <code>FULL</code>: All housing units have air conditioning
- <code>PARTIAL</code>: At least one housing unit has air conditioning
- <code>NONE</code>: No housing units have air conditioning
- <code>NA</code>: No document was available to determine AC status 


## Indoor temperature logs
The [indoor-temperatures](https://github.com/reuters-graphics/graphics_2025-prison-hvac-records/tree/main/indoor-temperatures) folder contains indoor temperature log data received from 5 states, with each state provided documents that were in their respective recording formats. 

For instance, the Texas Department of Criminal Justice provided daily temperature data taken at 3 p.m. in housing areas without air conditioning, while data for areas with air conditioning was collected at 1 p.m. every few days.

The California Department of Corrections and Rehabilitation provided temperature records from May through September 2024 in the form of scanned PDFs containing handwritten entries. In total, 189 PDFs comprising over 28,000 pages were given to Reuters. Of those, Reuters identified 20,326 pages as directly related to internal temperatures.

We focused on processing information from California as some CDCR facilities were in the nation’s top 10 most heat-exposed prisons, where average outdoor daily temperatures exceeded 85 degrees Fahrenheit (29 degrees Celsius) for multiple days in a row. California state prisons were also where most of the incarcerated individuals we interviewed were located.

To expedite processing this large volume of data, Reuters used [Gemini 2.5 Pro](https://deepmind.google/models/gemini/pro/), Google’s most advanced AI thinking model, to read and extract the temperature log information, outputting the results in JSON format.

Each page of the PDF was uploaded to Gemini 2.5 Pro along with a set of detailed instructions for data extraction. The AI-extracted data was then manually cleaned and merged into a single dataset. We further filtered this dataset to include internally recorded temperatures from June through August 2024. To find out more about how Reuters validated the accuracy of the AI-extracted data, please check out the [methodology](https://www.reuters.com/world/us/how-reuters-collected-analyzed-prison-temperature-data-2025-07-30/).

## Folder structure

- `air-conditioning`: Contains a single standardized spreadsheet with the responses on the presence of air conditioning in housing units. Each state folder contains the response from the respective department of corrections.

- `indoor-temperatures`: Contains indoor temperature log data received from 5 states, with each state providing documents in their respective recording formats.


## Contribution 
All data and methodology are publicly available for use, with a Reuters citation. 
