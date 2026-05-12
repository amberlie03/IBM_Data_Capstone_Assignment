# Data-Capstone
## Background
SpaceX is one of the most successful companies for affordable space travel. SpaceX advertises the Falcon9 rocket launches as 62 million dollars, whereas other providers cost upwards of 165 million dollars each. The reason for this price difference is that the first stage of launching can be reused. Therefore, if we determine whether the first stage will land, we can determine the cost of the launch. The goal of this project is to use the public information and training a machine learning model to predict if SpaceX will land successfully and reuse the first stage.

## Objectives 
The research attempts to identify the factors for a successful rocket landing.
- Analyse how features such as payload mass, launch site, flight number, and orbit type affect landing success.
- Explore trends in landing success over time.
- Build and evaluate machine learning models for binary classification of successful and unsuccessful landings.

## Skills 🧠
Data collection using SpaceX REST API and web scraping techniques.
Data wrangling and feature engineering.
Exploratory data analysis (EDA) with data visualization techniques, considering payload, launch site, flight number, and yearly trend.
SQL-based data analysis, calculating total payload, payload range for successful launches, and total number of successful and failed outcomes.
Geospatial visualisation with maps of launch sites.
Machine learning model development and evaluation using logistic regression, support vector machine (SVM), decision tree, and K-nearest neighbour (KNN). 

## Tools ⚙️
- Python (pandas, numpy, scikit-learn)
- Visualisations using matplotlib, seaborn, plotly, folium
- Web scraping: BeautifulSoup, requests
- SpaceX REST API
- Plotly Dash
- SQL

## Data Collection 📈
### API
- Retrieved the launch data using SpaceX REST API.
- JSON responses were parsed into structured DataFrames.
- Data filtered for Falcon 9 launches only.
### Web Scraping
- Requested Falcon 9 data from static url.
- Created a BeautifulSoup object from the HTML response to extract and parse additional launch data.
- Converted data into DataFrames.

## Data Wrangling 🧹
- Converted landing outcomes into binary values where 1 = success, 0 = failure.
- Handled missing values using the means of columns.
- Cleaned and merged datasets from different sources.

## Exploratory Data Analysis 🔎
### Key Findings using SQL queries
- Launch site success rate increased over time.
- KSC LC-39A has the highest success rate among landing sites.
- Orbits ES-L1, GEO, HEO, and SSO have 100% success rate.
- In general, the higher the payload mass, the better the landing outcome.
### Visualisation
- Most launches are close to the equator and coastlines, further from cities.
- There are clear relationships between payload, orbit type, and landing success.

## Geospatial Analysis 🗺️
- Maps to visualise launch sites were created using Folium maps.
- Proximity to coastlines, cities, and geographical features were analysed.
- Success rates compared by location.

## Dashboard 📊
An interactive dashboard was built using Plotly Dash, such as a pie chart of successful vs unsuccessful launches. Another example is a scatter plot of payload mass vs landing site success by booster version.

## Machine Learning Models 🤖 
Models included:
- Logistic Regression
- Support Vector Machine (SVM)
- Decision Tree
- K-Nearest Neighbours (KMM)
### Model Methodology
1. Standardised features using StandardScaler.
2. Data was split into training and test sets.
3. GridSearchCV was used to refine parameters.
4. Models were evaluated using accuracy, F1 score, and Jaccard score.

## Results
- All models performed similarly on the test set.
- The decision tree achieved the highest accuracy overall.
- Model performance confirms strong relationships between landing success and selected features.

## Conclusion
- Decision Tree was the best algorithm model for this data.
- Launch success has increased significantly over time.
- Launch site and orbit type are key predictors of success.
- Payload mass shows a positive relationship with landing success.
- Most launches occur near coastlines and equatorial regions.

## Future Improvements
- Incorporate additional real-time or external datasets.
- Experiment with more advanced models.
- Improve predictive performance.


