## Folder structure

Each state folder contains the response from the respective department of corrections.

## Data dictionary

Variable name | Definition
------------- | ----------
`facility_id` | A unique id from the [Homeland Infrastructure Foundation Level Data (HIFLD) database](https://hifld-geoplatform.hub.arcgis.com/datasets/geoplatform::prison-boundaries-1/about) 
`prison_name` | Name of the facility
`ac_status`   | Indicates whether at least one housing unit has air conditioning. Possible values: <br>• `YES`: At least one housing unit has air conditioning. This includes both mechanical air conditioning and evaporative cooling systems, commonly known as swamp coolers. <br>• `NO`: No housing units have air conditioning. <br>• `NA`: No document was available to determine AC status.
`ac_status_details` | Additional information on AC coverage. Possible values: <br>• `Full`: All housing units have AC <br>• `Partial`: At least one housing unit has AC <br>• `None`: No housing units have AC <br>• `NA`: No documentation available
`address` | Street address of the facility
`city` | City where the facility is located
`state` | Two-letter state abbreviation
`zip` | ZIP code of the facility

