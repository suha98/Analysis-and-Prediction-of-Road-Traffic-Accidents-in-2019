# Analysis-and-Prediction-of-Road-Traffic-Accidents-in-2019

From 2017 to 2020, over 6 million casualties were recorded in the U.K. as a consequence of road traffic accidents (Reported  road  casualty  statistics  in  great  britain:  Interactive  dashboard .  2022). By using accident, vehicle, and casualty data from the U.K. government in 2019, and associated data  on  the  involved  vehicles  and  casualties, a model to predict accident severity was developed in this project, from a series of associated factors. Prediction results using stacked and hypertuned machine learning algorithms have been presented, and finally, recommendations presented to resolve the identified issues.  

Below is a summary of the methodologies implemented in this project:

## Preprocessing 

1. Imputation of missing values such as vehicle ages (including those of horses and public transport)
2. Removing outliers in engine capacity, driver ages etc.
3. Feature Engineering by adding columns from dates such as day of week and month

## Analysis

Correlations were analysed between:

1. Accident frequency and time of day
2. Accident frequency and day of week
3. Accident frequency and day of month
4. Accident frequency and month
5. Vehicle type and accident frequency
6. Accident frequency on celebratory days such as Christmas and New Year's
7. Accident frequency and daylight hours
8. Accident frequency and Casualty Type
9. Accident frequency and Weather
10. Accident frequency and driver age
11. Accident severity and speed limit
12. Accident severity and weather
13. Accident severity and road conditions
14. Accident severity and proximity of accident to a crossing
15. Accident frequency and location of accident (using K-Means clustering)
16. Accident severity and journey purpose of driver
17. Accident severity and driver age
18. Accident severity and driver gender
19. Casualty frequency and driver age
20. Casualty frequency and vehicle type
21. Casualty frequency and home area type of driver
22. Casualty frequency and driver age

## Feature Selection

Feature selection was done with the SelectKBest algorithm and three functions ANOVA (fclassif) for numerical columns, Mutual Information Classifier, and Chi Square (categorical columns). After encoding the selected features and balancing the output variable, the grid search algorithm was implemented on a sample of the dataset to hypertune parameters for six machine learning models.

## Machine Learning Models

Five main machine learning models were implemented: Logistic Regression, Decision Tree, Random Forest, K Nearest Neighbours, and XGBoost. The sixth model was a stacked version of the five with their hypertuned versions as Layer 0 and Logistic Regression as Layer 1. Scikit Learn's pipelines were used in order to build these models with grid search and then stack them.

## Recommendations

The following measures were recommended to reduce accident numbers in the future: 

1. Increasing and improving public transport measures (like buses and trams), to encourage people 
to use them in place of cars – the former is far safer with only several thousand accidents, 
compared to over 1.5 million car accidents. 
2. Employing lollipop men/ladies at all pedestrian crosses in major cities and roads during rush 
hours, to reduce pedestrian casualties. 
3. Deploying crossings (zebra, puffin, pelican etc.) in regions where there are none available within 
50metres to reduce pedestrian casualties. 
4. Creatively utilizing social media platforms to educate on road safety – especially during summer 
months, people need to be reminded of the dangers. 
5. Deploy a minimum age for children riding horses on the road during which they must have adult 
supervision. 


