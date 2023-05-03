# Campbell_Rooney_ENV872_EDASp23_FinalProject

Final project for Spring 2023 Environmental Data Analytics course at the Nicholas School of the Environment at Duke University. 

1. County Boundary Data: In order to first map county lines onto our state of interest, we downloaded cartographic boundary shapefiles from the US Census Bureau website. The most recent year for these files was 2022. We used the 20m resolution file. Files were downloaded from the following URL: <https://www.census.gov/geographies/mapping-files/time-series/geo/cartographic-boundary.html>. 

2. HUC12 Boundary Data: Because our wind energy data was at the HUC12 geographic level, we needed to download a cartographic boundary shapefile on HUC12s in Wyoming to then be able to assign HUC12 geography and wind energy figures to Wyoming counties. This would enable us to then do our comparative analysis with SVI and power plants at the county level. HUC12 data was last updated in 2019 and comes from the Wyoming Geospatial Hub of the Wyoming Water Development Office. We downloaded this shapefile from the following URL: <https://water.geospatialhub.org/datasets/687dadd8b93f4ad092b64a84caf5b72a_0/explore?location=42.808013%2C-107.387472%2C6.66>.

3. The Social Vulnerability Index data was downloaded from the US Center for Disease Control Agency for Toxic Substances and Disease Registry website. The most recent year for which data is available is 2020. The geography selected was Wyoming, and the geography type was counties. We downloaded data as both shapefiles and csv file types, ultimately using the csv file. Data was pulled from the following URL: <https://www.atsdr.cdc.gov/placeandhealth/svi/data_documentation_download.html>. Additional documentation for the data was found here: <https://www.atsdr.cdc.gov/placeandhealth/svi/documentation/SVI_documentation_2020.html>. 

4. Homeland Infrastructure Foundation-Level Data (HIFLD) was read directly into R using their open data site as geojson data. The link used for this project was <https://opendata.arcgis.com/datasets/ee0263bd105d41599be22d46107341c3_0.geojson>.

5. Wind energy data estimated at the HUC 12 level was read directly into R from the Environmental Protection Agency's EnviroAtlas data available online using the following URL: <https://raw.githubusercontent.com/ENV859/EnviroAtlasData/main/Wind_Energy.csv>.
