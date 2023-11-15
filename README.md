# Google mobility Analysis

The Global Mobility Report (GMR) dataset contains information about people’s movement during the COVID-19 pandemic for over 130 countries from the year 2020 to 2022. The reports recorded movement trends over time, across different categories of places such as retail and recreation, groceries and pharmacies, parks, transit stations, workplaces, and residential. The dataset was downloaded from [Google mobility data](https://www.google.com/covid19/mobility/).

The dataset uses baseline values, which are computed based on historical data from a significant period before the pandemic for comparison. These baseline values are presented as positive and negative percentage  values, indicating an increase and decrease in visits compared to the baseline respectively. The data format ranges from text, numerical and date.

The columns are briefly defined below:
1. Country region code: The two-letter code representing the country or region.
2. Country region: The name of the country or region
3. Sub-region 1: First-level administrative subdivision (e.g., state, province) within the country or region.
4. Subregion 2: Second-level administrative subdivision (e.g., county, district) within the first-level subdivision.
5. Metro area: The name of the metropolitan area
6. Iso_3166_2_code: The ISO 3166-2 code representing the country or region.
7. Census fips code The FIPS code represents the country or region
8. Place ID: Unique ID for each sub-region.
9. Date: The timestamp indicates the specific date of the data point.
10. Retail and recreation per cent change from baseline: Percentage change in visits to retail and recreation places compared to a baseline period.
11. Grocery and Pharmacy per cent change from baseline: Percentage change in visits to grocery and pharmacy places compared to a baseline period.
12. Parks per cent change from baseline: Percentage change in park visits compared to a baseline period.
13. Transit stations per cent change from baseline: Percentage change in visits to transit stations compared to a baseline period.
14. Workplaces per cent change from baseline: Percentage change in visits to workplaces compared to a baseline period.
15. Residential per cent change from baseline: Percentage change in visits to residential areas compared to a baseline period.
    
For this analysis, the following columns will be dropped because of their little to no relevance 
to the task—country region code, country region, metro area, iso_3166_2_code, Census fips
code and place ID.

This analysis was done to analyse  how people’s mobility contributes immensely to the spread and/or reduction of the disease in Australia. This in turn will shed light on how to combat other pandemics in the future. It will also help to understand the mobility trend before and after vaccination and monitor the trend with various economic activities.

## Analysis

The analysis was done on Azure virtual machine and with Pymongo

The following steps were taken to select the useful subset of the dataset.
1. Locate the data on the mobaxterm using cd location of the file.
2. import the data using mongo import into a “gmr” database and “Mobility” collection
3. Launch mongosh
4. Access the data on MongoDB to confirm it has been imported
5. Connected the database with google colab
6. Imported the dataset into the created database.
7. Viewed the dataset to understand the contents.
8. Selected only datasets that are for Australia and saved in a new collection called Australia.
9. Dropped irrelevant fields
10. Renamed relevant fields for easy access
11. Selected data for each city in Australian states and named them accordingly.
12. Access the data for each city using Pandas and NumPy to preprocess and remove missing values
