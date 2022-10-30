# Capstone_Project

## Team 6:
Alison Cook- Square

Michael Fischer- Circle

Rafael Silva-Almodovar- Triangle

Contacts: Slack, Zoom meeting study sessions in class

## Overview/ Purpose
Reviewing Kaggle Dataset for Climate Change: Earth Surface Temperature, and Eighty years of Canadian climate data to predict climate changes for 3 major cities (Lagos, Montreal, and Shianghai)
1- Cleaning the datasets to remove years prior to 1900 then narrowing down from 2000-2013, dropping NaN, filtered for Northern Hemispheres and further broken down by 3 cities data only.

2- Splitting data into tables using SQLalchemy/PgAdmin.

3- Supervised machine learning models with process (load data and drop un-necessary columns), train (50% data), test (50% data), predict() and include results (accuracy r-squared 99%) and why choose specific model[linear regression and random forest classifier(top items)], 

4- Visulazation answering questions and dashboard items(interactive(dashboard buttons) and static(tableau))


Questions to answer:

1- Will the 2000-2013 weather trends indicate an increase in Earth surface temperature for Lagos, Nigeria; Shanghai, China and Montreal, Canada?

2- What are the global increases in average temperature over time?

3- Do major cities impact climate change heavier?

4- Does relation to the equator have an effect?

5- What model would best predict future climate change? 


## Resources and References
Kaggle Dataset: Climate Change: Earth Surface Temperature Data (https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data?resource=download)
GlobalTemperatures.csv, GlobalTemperaturesByCountry.csv, GlobalTemperaturesByMajorCity.csv

Kaggle Dataset: Eighty years of Canadian climate data (https://www.kaggle.com/datasets/aturner374/eighty-years-of-canadian-climate-data)

SQLalchemy/pgAdmin

Jupyter Notebook

Tableau

Google Slides: https://docs.google.com/presentation/d/1-z85JcXZvhZiptGr7-FeUXKVXUaN76JUyfb_Ot5wezs/edit#slide=id.g1727fbf119b_0_35

Supervised Machine Learning


## Results
Data cleaning: 
	Reviewed Data:
		Types pf data in each column
		Check for unique values
		Counts for values
	Filtering for Northern Hemisphere data only
	Dropped the Null values
	LOC filtered data for only year 1900CE-2013CE
	Create sample data sets and convert to CSV file

ERD- Connecting data sets by Datetime (dt) and City (city) for use in database and model testing

Database

Supervised Machine Learning: Linear regression and Random Forest Classification

	This dataset contains 10 columns which means we are dealing with irrelevant content.

	Droped the non-beneficial columns such as 'Unnamed: 0', 'LandAverageTemperatureUncertainty', 'LandMaxTemperatureUncertainty', 'LandMinTemperatureUncertainty', 'LandAndOceanAverageTemperatureUncertainty' for machine learning process.
	
	Unnamed column was dropped as it is a secondary index column and not needed for testing. 
	
	All Uncertainty colums were dropped since they dont have clear contributions to the average data we are testing.

	After the pre-processing, the dataset now contains 5 data relative columns.

Dashboard/Visualization
	

## Summary/ Improvements
 Improvments for future data testing, locate cities closer to ocean temperature affected bodies of water (large lakes or icebergs), would increase data availabe for more accurate predictive modeling. 
[Recommendation: multiple linear regression 
whats next? what did we learn? and why do we care about what we learned? if water temperature was removed, or only tested on land locked states?]