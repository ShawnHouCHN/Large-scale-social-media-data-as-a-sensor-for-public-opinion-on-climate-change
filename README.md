# Large-scale-social-media-data-as-a-sensor-for-public-opinion-on-climate-change
This is the source code repository of master thesis for Xiaoshen Hou to obtain Master of Science in Digital Media Engineering at DTU 

## 1. Project Structure: 
The project consists of three sections, data ingestion, data aggregation/enrichment and modelling.
- Data Ingestion 
  - Datasets
    1. Twitter is retrieved from authenticated resouce via Spark application.
    2. Meteorological data including PRISM and NCEP Reanalysis 2 are downloaded from public resource
    3. Population density is given by NASA.
    4. US county details is also public on US Census Bureau
  - Temporal Period
    2013 - 2016
  - Geographical Region
    Contiguous US
   
  The "preprocessing" notebook contains the integration process of twitter and meteorological data and priliminary analysis.

- Data Aggregation/Enrichment. 
  At this step, notebooks are managed accoundingly for each year due to the complexity of computation
  - Aggregation
  The "binned" and "county" notebook respectively contain distinct granularity torwards the processed data. The "binned" one applies 25KM and 50KM raster over US while the "county" one confines each oberservation to a county.
    
