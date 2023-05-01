# Campbell_Rooney_ENV872_EDASp23_FinalProject

Final project for Spring 2023 Environmental Data Analytics course at the Nicholas School of the Environment at Duke University. 

1. County Boundary Data: In order to first map county lines onto our state of interest, we downloaded cartographic boundary shapefiles from the US Census Bureau website. The most recent year for these files was 2022. We used the 20m resolution file. Files were downloaded from the following URL: <https://www.census.gov/geographies/mapping-files/time-series/geo/cartographic-boundary.html>. 

2. The Social Vulnerability Index data was downloaded from the US Center for Disease Control Agency for Toxic Substances and Disease Registry website. The most recent year for which data is available is 2020. The geography selected was Wyoming, and the geography type was counties. We downloaded data as both shapefiles and csv file types, ultimately using the csv file. Data was pulled from the following URL: <https://www.atsdr.cdc.gov/placeandhealth/svi/data_documentation_download.html>. Additional documentation for the data was found here: <https://www.atsdr.cdc.gov/placeandhealth/svi/documentation/SVI_documentation_2020.html>. 

3. Homeland Infrastructure Foundation-Level Data (HIFLD) was read directly into R using their open data site as geojson data. The link used for this project was <https://opendata.arcgis.com/datasets/ee0263bd105d41599be22d46107341c3_0.geojson>.

4. Wind energy data estimated at the HUC 12 level was read directly into R from the Environmental Protection Agency's EnviroAtlas data available online using the following URL: <https://raw.githubusercontent.com/ENV859/EnviroAtlasData/main/Wind_Energy.csv>.