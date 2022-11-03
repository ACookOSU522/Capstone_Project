# Capstone_Project

## Team 6:
<<<<<<< HEAD
Alison Cook- Square

Michael Fischer- Circle

Rafael Silva-Almodovar- Triangle

Contacts: Slack, Zoom meeting study sessions in class
=======
Alison Cook- Square (Dashboard/Slides/Tableau)

Michael Fischer- Circle (Data Cleaning/Database)

Rafael Silva-Almodovar- Triangle (Modeling)

Kelli Magsig- X (Presentation)

Contacts/Communication: Slack, Zoom meeting study sessions in class

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
# Capstone_Project

## Team 6:
Alison Cook- Square (Dashboard/Slides/Tableau)

Michael Fischer- Circle (Data Cleaning/Database)

Rafael Silva-Almodovar- Triangle (Modeling)

Kelli Magsig- X (Presentation)

Contacts/Communication: Slack, Zoom meeting study sessions in class
>>>>>>> 53541e34514c738cdb720fc9e5fce28e60f06e24

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

Supervised Machine Learning:
- Preliminary feature engineering and preliminary feature selection, including decision-making process.

- Out of the data that was left after pre-processing, we found that the most relevant columns to determine land and ocean average temperature are "LandAverageTemperature", "LandMaxTemperature", and, "LandMinTemperature". We also found that it did not make sense to use "LandAndOceanAverageTemperature" to predict any of the other variables, so we made this our target variable. Considering the data we had included features and targets, the best way to map the data was through supervised machine learning.

Description of how data was split into train and test set

- Considering we have about 1992 rows of data after pre-processing, we found that training about 75% of the data, to then test on 25% of the data was the best split.

Model choice including advantages and disadvantages

- Since our target value is continuous, we decided that a multiple linear regression model was best. The advantages associated with this model include being simple to implement, the algorithm works best when there is a clear linear relationship between the dependent and independent variables. Some disadvantages include that it assumes a straight-line relationship between independent and dependent variables, it does not take into account the attributes involved, outliers can have great impact on the data, and since linear regression looks at the relationship between the mean of the variables, the whole story and description of variables is not being told. 


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
<<<<<<< HEAD

Database
=======
![QuickDBD-Free Diagram (1)](https://user-images.githubusercontent.com/106544424/199624648-d2bca78f-635f-4b54-a92a-d4895a09ca37.png)

Database
![Capture](https://user-images.githubusercontent.com/106544424/199624661-3b35a639-209a-484e-a04d-b8ac86e493a5.PNG)
>>>>>>> 53541e34514c738cdb720fc9e5fce28e60f06e24

Supervised Machine Learning: Linear regression and Random Forest Classification

	This dataset contains 10 columns which means we are dealing with irrelevant content.

	Droped the non-beneficial columns such as 'Unnamed: 0', 'LandAverageTemperatureUncertainty', 'LandMaxTemperatureUncertainty', 'LandMinTemperatureUncertainty', 'LandAndOceanAverageTemperatureUncertainty' for machine learning process.
	
	Unnamed column was dropped as it is a secondary index column and not needed for testing. 
	
	All Uncertainty colums were dropped since they dont have clear contributions to the average data we are testing.

	After the pre-processing, the dataset now contains 5 data relative columns.

<<<<<<< HEAD
Dashboard/Visualization
	
=======
Dashboard with Interactive Tableau Story and GIF Visualization
	
![Tableau trend model](https://user-images.githubusercontent.com/106544424/199624753-4d85f91b-fbde-4911-a330-3345f1383798.png)
>>>>>>> 53541e34514c738cdb720fc9e5fce28e60f06e24

## Summary/ Improvements
 Improvments for future data testing, locate cities closer to ocean temperature affected bodies of water (large lakes or icebergs), would increase data availabe for more accurate predictive modeling. 
[Recommendation: multiple linear regression 

<<<<<<< HEAD
whats next? what did we learn? and why do we care about what we learned? if water temperature was removed, or only tested on land locked states?]
=======

whats next? what did we learn? and why do we care about what we learned? if water temperature was removed, or only tested on land locked states?]
>>>>>>> 53541e34514c738cdb720fc9e5fce28e60f06e24
