# Capstone_Project

## Team 6:
Alison Cook- Square (Dashboard/Slides/Tableau)

Michael Fischer- Circle (Data Cleaning/Database)

Rafael Silva-Almodovar- Triangle (Modeling)

Kelli Magsig- X (Presentation)


## Overview/ Purpose
### Data selected in an effort to learn degree of global warming based on latitude 

Reviewing Kaggle Dataset for Climate Change: Earth Surface Temperature, and Eighty years of Canadian climate data to predict climate changes for 3 major cities (Lagos, Montreal, and Shianghai)

1- Cleaning the datasets to remove years prior to 1900 then narrowing down from 2000-2013, dropping NaN, filtered for Northern Hemispheres and further broken down by 3 cities data only.

2- Splitting data into tables using SQLalchemy/PgAdmin.

3- Supervised machine learning models with process (load data and drop un-necessary columns), train (50% data), test (50% data), predict() and include results (accuracy r-squared 99%) and why choose specific model: linear regression and random forest classifier. 

4- Dashboard visualizations answering questions


### Questions to answer:

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
- Types of data in each column
![Capture](https://user-images.githubusercontent.com/106544424/201540347-870c9177-50f4-43d4-9bdb-0e30c17f8899.PNG)

- Check for unique values
- Counts for values
- Filtering for Northern Hemisphere data only
![countries_no_cords](https://user-images.githubusercontent.com/106544424/201540392-c40002e7-0a35-4de8-875d-683396cdfada.PNG)

- Dropped the Null values
- LOC filtered data for only year 1900CE-2013CE
![date time format](https://user-images.githubusercontent.com/106544424/201540332-c48322c0-8445-459a-9612-fbb436fca115.PNG)

Create sample data sets and convert to CSV file
![merging data](https://user-images.githubusercontent.com/106544424/201540335-64b435db-4662-4ea3-8418-6154438f2b59.PNG)


ERD
- Connecting data sets by Datetime, Country, Average Temperature and City for use in database and model testing
![final ERD](https://user-images.githubusercontent.com/106544424/201540239-6b50e348-8fff-44fe-a45c-b18d2b195a5c.png)

Database
1- Identified unnecessary data points
2- Narrowed the scope of the analysis
3-Created a workable database with SQLalchemy using master data sets and cleaned version

![Capture](https://user-images.githubusercontent.com/106544424/199624661-3b35a639-209a-484e-a04d-b8ac86e493a5.PNG)
![SQL_Database](https://user-images.githubusercontent.com/106544424/202060493-d320a47b-6b49-4f79-a21a-d796d945686e.png)


### Supervised Machine Learning: Linear regression and Random Forest Classification:

1- Preliminary feature engineering and preliminary feature selection, including decision-making process.
	- Unnamed column was dropped as it is a secondary index column and not needed for testing. 	
		- All Uncertainty colums were dropped since they do not clearly contribute to the average data we are testing.
2- Out of the data that was left after pre-processing, we found that the most relevant columns to determine land and ocean average temperature are "LandAverageTemperature", "LandMaxTemperature", and, "LandMinTemperature". We also found that it did not make sense to use "LandAndOceanAverageTemperature" to predict any of the other variables, so we made this our target variable. 
	- Considering the data we had included features and targets, the best way to map the data was through supervised machine learning.
	
3- Description of how data was split into train and test set
	- Early machine modeling tested on 25% of data with pipeline linear regression MAE 0.1567, and Random Forest Model MAE 0.1355, testing r-squared of 97.67%, and 98.04% for RFR.
	- Considering we have about 1992 rows of data after pre-processing, we found that training about 75% of the data, to then test on 25% of the data was the best split.

4- Model choice including advantages and disadvantages
	- accuracy score r-square = Linear Regression - 97.67, RFR - 98.04%
	- Since our target value is continuous, we decided that a multiple linear regression model was best. 
	- The advantages associated with this model include being simple to implement, the algorithm works best when there is a clear linear relationship between the dependent and independent variables. 
	- Some disadvantages include that it assumes a straight-line relationship between independent and dependent variables, it does not take into account the attributes involved, outliers can have great impact on the data.
	- Since linear regression looks at the relationship between the mean of the variables, the whole story and description of variables is not being told. 
	- For random forest some advantages include reduced overfitting in decision tree, its flexible to both classification and regression problems, works with categorical and continuous variable, normalization is not required, and it automates missing values present in data. Some disadvantages include needing extra computational power due to numerous trees it builds, it requires more time for training data, and it fails to determine the significance of each value.
![LinearReg](https://user-images.githubusercontent.com/106544424/201238944-977cc328-b8b6-4600-bde5-0b8667d9d9a8.png)
 

### Dashboard with Interactive Tableau Story and Carousel Visualization
Dashboard created to show increase in temperatures with sliding carousel specific to 13 year data set, highlighting global temperature increase. Also showcasing Supervised Learning linear model trend
![Dash 11922](https://user-images.githubusercontent.com/106544424/201239187-a84e16a8-313d-4ae4-bc2a-02d71fbbe769.png)

Interactive Tableau charts with pop-ups to illustrate locatin specific charts of annual overall temperature increase
![Dash 11922-2](https://user-images.githubusercontent.com/106544424/201239201-8d2d825c-c440-48b7-b9d7-0d9d76b92f91.png)
	
![Tableau trend model](https://user-images.githubusercontent.com/106544424/199624753-4d85f91b-fbde-4911-a330-3345f1383798.png)


## Summary/ Improvements
### Summary:
1- Will the 2000-2013 weather trends indicate an increase in Earth surface temperature for Lagos, Nigeria; Shanghai, China and Montreal, Canada? Yes, accurate data representation for supporting an observed increase in overall global temperature.

2- What are the global increases in average temperature over time? Montreal +3.0%(4.2M), Lagos +0.4% increase (14.8M), Shanghai +1.5%(27.8M). 

3- Do major cities impact climate change heavier? Population did not have an effect on Montreal +3.0%(4.2M), Lagos +0.4% increase (14.8M), Shanghai +1.5%(27.8M). 

4- Does relation to the equator have an effect? No, average temperature was a slower increase over time period at equator location. 

5- What model would best predict future climate change? The random forest regressor model seemed best to test for the data given. If the variables were to change, the model used may need to be revised. 

### Improvements:
-Locate additional cities near ocean temperature affected bodies of water (large lakes or icebergs), would increase data available for more accurate predictive modeling. 

-Utilize humidity as a measured data set to check for fluctuation in results.

-Retest data for areas prone to impactful weather patterns (fires, hurricanes, tornados, floods)and see if they indicate increase temperature trends.

