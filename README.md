# Data-Capstone
## Background
SpaceX is one of the most successful companies for affordable space travel. SpaceX advertises the Falcon9 rocket launches as 62 million dollars, whereas other providers cost upwards of 165 million dollars each. The reason for this price difference is that the first stage of launching can be reused. Therefore, if we determine whether the first stage will land, we can determine the cost of the launch. The goal of this project is to use the public information and training a machine learning model to predict if SpaceX will land successfully and reuse the first stage.

## Objectives
The research attempts to identify the factors for a successful rocket landing.
- Analyse how features such as payload mass, launch site, flight number, and orbit type affect landing success.
- Explore trends in landing success over time.
- Build and evaluate machine learning models for binary classification of successful and unsuccessful landings.

## Skills
Data collection using SpaceX REST API and web scraping techniques.
Data wrangling and feature engineering.
Exploratory data analysis (EDA) with data visualization techniques, considering payload, launch site, flight number, and yearly trend.
SQL-based data analysis, calculating total payload, payload range for successful launches, and total number of successful and failed outcomes.
Geospatial visualisation with maps of launch sites.
Machine learning model development and evaluation using logistic regression, support vector machine (SVM), decision tree, and K-nearest neighbor (KNN). 

## Tools 
- Python (pandas, numpy, scikit-learn)
- Visualisations using matplotlib, seaborn, plotly, folium
- Web scraping: BeautifulSoup, requests
- SpaceX REST API
- Plotly Dash
- SQL

## Data Collection
### API
Retrieved the launch data using SpaceX REST API.
JSON responses were parsed into structured DataFrames.
Data filtered for Falcon 9 launches only.
### Web Scraping
Requested Falcon 9 data from static url.
Created a BeautifulSoup object from the HTML response to extract and parse additional launch data.
Converted data into DataFrames.

## Data Wrangling
Converted landing outcomes into binary values where 1 = success, 0 = failure.
Handled missing values using the means of columns.
Cleaned and merged datasets from different sources.

## Exploratory Data Analysis
### Key Findings
- Launch site success rate increased over time.
- KSC LC-39A has the highest success rate of launches.
- Orbits ES-L1, GEO, HEO, and SSO have 100% success rate.
- In general, the higher the payload mass, the better the landing outcome.

### Visualisation
- Most launches are close to the equator and coastlines, further from cities.
- There are clear relationships between payload, orbit type, and landing success.


# Exploratory Data Analysis:
Launch success has improved over time
KSC LC-39A has the highest success rate among landing sites
Orbits ES-L1, GEO, HEO, and SSO have a 100% success rate
# Visualization / Analytics:
Most launch sites are near the equator, and all are close to the coast
# Predictive Analytics
All models performed similarly on the test set. The decision tree model slightly outperformed in accuracy
# Methodology
Request rocket launch data from API
Decode the response and turn into a data frame using .json_normalize()
Request info by applying custom functions
Construct data into a dictionary and create a data frame from it
Filter the data for Falcon 9 
Replace missing values with the column mean
Export the data to CSV


# EDA with Visualization
Create charts to analyze relationships and show comparisons
# EDA with SQL
Query the data to understand more about the data
# Maps with Folium
Create maps to visualize launch sites, view launch outcomes and see distance to proximities
# Dashboard with Plotly Dash
Create dashboard
Pie chart showing successful launches
Scatter chart showing Payload Mass vs. Success Rate by Booster Version
# Predictive Analytics
Create NumPy array from the Class column
Standardize the data with StandardScaler. Fit and transform the data.
Split the data using train_test_split
Create a GridSearchCV object for parameter optimization
Apply GridSearchCV on different algorithms: logistic regression, support vector machine, decision tree, K-Nearest Neighbor
Calculate accuracy on the test data for all models
Assess the confusion matrix for all models
Identify the best model using Jaccard_Score, F1_Score and Accuracy
# Conclusion
Decision Tree is the best algorithm model for this data 


