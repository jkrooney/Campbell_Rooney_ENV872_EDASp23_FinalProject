# Campbell_Rooney_ENV872_EDASp23_FinalProject

## Summary
Final project for Spring 2023 Environmental Data Analytics course at the Nicholas School of the Environment at Duke University. 

This repository contains data on Wyoming county boundaries and Wyoming HUC12 boundaries, Wyoming Social Vulnerability Index, Wyoming power plant locations and fuel types, and Wyoming wind energy. The purpose is to assess relationships between socially vulnerable communities and the current presence of power plants, and future potential for wind energy generation in such communities. Our goals for analysis are to map this data spatially, to use plots to assess which counties have the greatest social vulnerability and wind energy potential, and to draw meaningful conclusions from this data analysis regarding future potential for wind energy generation in communities that are socially vulnerable and currently depend on fossil fuel power plants. 

## Investigators
Sam Campbell and John Rooney
Master of Environmental Management students at Duke University's Nicholas School of the Environment
sam.campbell@duke.edu
john.rooney@duke.edu 

## Keywords
Wind, Energy, Social Vulnerability Index, Poverty, Power plants, IRA

## Database Information
1. County Boundary Data: In order to first map county lines onto our state of interest, we downloaded cartographic boundary shapefiles from the US Census Bureau website. The most recent year for these files was 2022. We used the 20m resolution file. Files were downloaded from the following URL: <https://www.census.gov/geographies/mapping-files/time-series/geo/cartographic-boundary.html>. Accessed 17 April 2023. 

2. HUC12 Boundary Data: Because our wind energy data was at the HUC12 geographic level, we needed to download a cartographic boundary shapefile on HUC12s in Wyoming to then be able to assign HUC12 geography and wind energy figures to Wyoming counties. This would enable us to then do our comparative analysis with SVI and power plants at the county level. HUC12 data was last updated in 2019 and comes from the Wyoming Geospatial Hub of the Wyoming Water Development Office. We downloaded this shapefile from the following URL: <https://water.geospatialhub.org/datasets/687dadd8b93f4ad092b64a84caf5b72a_0/explore?location=42.808013%2C-107.387472%2C6.66>. Accessed 17 April 2023.

3. The Social Vulnerability Index data was downloaded from the US Center for Disease Control Agency for Toxic Substances and Disease Registry website. The most recent year for which data is available is 2020. The geography selected was Wyoming, and the geography type was counties. We downloaded data as both shapefiles and csv file types, ultimately using the csv file. Data was pulled from the following URL: <https://www.atsdr.cdc.gov/placeandhealth/svi/data_documentation_download.html>. Additional documentation for the data was found here: <https://www.atsdr.cdc.gov/placeandhealth/svi/documentation/SVI_documentation_2020.html>. Accessed 17 April 2023.

4. Homeland Infrastructure Foundation-Level Data (HIFLD) was read directly into R using their open data site as geojson data. The link used for this project was <https://opendata.arcgis.com/datasets/ee0263bd105d41599be22d46107341c3_0.geojson>. Accessed 26 April 2023.

5. Wind energy data estimated at the HUC 12 level was read directly into R from the Environmental Protection Agency's EnviroAtlas data available online using the following URL: <https://raw.githubusercontent.com/ENV859/EnviroAtlasData/main/Wind_Energy.csv>. Accessed 17 April 2023.

## Folder structure, file formats, and naming conventions 
The repository contains folders for code written by the investigators, relevant lessons from the course (Spatial Analysis and Crafting Reports), Data, and the official Project files (final report and README). The Data folder contains further subfolders for Spatial, Raw, and Processed data.

Code is written in RMD files and knitted as an HTML file to display maps that use the 'mapview()' function. Spatial data uses .shp files, and non-spatial data uses .csv files. 

## Metadata
1. County Boundary Data
  Columns: STATEFP (chr), COUNTYFP (chr), COUNTYNS (chr), AFFGEOID (chr), GEOID (chr), NAME (chr), NAMELSAD (chr), STUSPS (chr), STATE_NAME (chr), LSAD (chr), ALAND (num), AWATER (num), geometry (sfc_MULTIPOLYGON)
  Units: N/A

2. HUC12 Boundary Data
  Columns: OBJECTID (int), TNMID (chr), MetaSource (chr), SourceData (chr), SourceOrig (chr), SourceFeat (chr), LoadDate (Date), GNIS_ID (int), AreaAcres (num), AreaSqKm (num), States (chr), HUC12 (chr), Name (chr), HUType (chr), HUMod (chr), ToHUC (chr), NonContrib (num), NonContr_1 (num), Shape_Leng (num), Shape_Area (num), geometry (sfc_POLYGON)
  Units: N/A, acres, square kilometers

3. Social Vulnerability Index data
  Columns: COUNTY (chr), FIPS (Factor), LOCATION (chr), E_TOTPOP (int), E_POV150 (int), E_MINRTY (int)
  Units: N/A

4. Homeland Infrastructure Foundation-Level Data
  Columns: OBJECTID (ing), PLANT_CODE (chr), NAME (chr), ADDRESS (chr), CITY (chr), STATE (chr), ZIP (chr), TELEPHONE (chr), TYPE (chr), STATUS (chr), COUNTY (chr), COUNTYFIPS (chr), COUNTRY (chr), LATITUDE (num), LONGITUDE (num), NAICS_CODE (chr), NAICS_DESC (chr), SOURCE (chr), SOURCEDATE (POSIXct), VAL_METHOD (chr), VAL_DATE (POSIXct), WEBSITE (chr), OPERATOR (chr), OPERAT_ID (chr), OPER_CAP (num), SUMMER_CAP (num), WINTER_CAP (num), PLAN_CAP (num), GEN_UNITS (num), PLAN_UNITS (num), PRIM_FUEL (chr), SEC_FUEL (chr), geometry (sfc_POINT)
  Units: N/A

5. Wind Energy Data
  Columns: NAME (chr), AvgWind (num), geometry (geometry)
  Units: GigaWatt Hours per Square Kilometer per Day

## Scripts and code
The code that the Investigators generated is contained in the Code and Project folders. The Code folder includes draft code generated throughout the data wrangling and analyisis process, and the Project folder contains final iterations of this code used to demonstrate and visualize the Investigators' findings. 

## Quality assurance/quality control
For quality assurance and quality control, we chose the most recent available years for our datasets from open sources. We checked for and removed NAs as needed, and mapped our spatial data to check that it appeared as we expected it would. 
