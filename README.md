# Large-scale-social-media-data-as-a-sensor-for-public-opinion-on-climate-change
This is the source code repository of master thesis for Xiaoshen Hou to obtain Master of Science in Digital Media Engineering from Technical University of Denmark. Supervisor is Professor Sune Lehmann and external advisor is phd researcher Kelton Minor. 

## Project Structure: 
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
  
  The "binned" and "county" notebook respectively contain distinct granularity torwards the processed data. The "binned" one applies 25KM and 50KM raster over US while the "county" one confines each oberservation to a county.
  
  Data is enriched by using DeepMoji project published by [MIT Media Lab Project](https://deepmoji.mit.edu/) to support the sentimental analysis of the observation in the project. This process has been put in Data Preprocessing DeepMoji.ipynb notebook in the repo
    
- Data Modelling.

  The empirical model is the multigroup fixed effect model, following the guideline from the paper: [weather impacts expressed sentiment](https://arxiv.org/abs/1709.00071), where weather factors act as covariates while tweet volume/ emotion scores are the dependent 
  variables. The temporal and spatial difference of oberservations behave as unobserved time-invariant variables correlated with the 
  regressor matrix. The analysis is documented in a R notebook and plots based on different granularities are saved in the repo.
