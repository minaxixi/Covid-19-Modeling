# Covid-19-Modeling

## Goal
This project is to model and visualize Covid-19 cases based on county-level demographic and economic dataset

## Data
- The Covid-19 data (from [JHU-CSSEGIS](https://github.com/CSSEGISandData/COVID-19))
- The geo-json data (from [Plotly](https://github.com/plotly/datasets))
- The US county-level demographics and economy data (from [US Census Bureau](https://www.census.gov/data.html))


## Exploratory Data Analysis
- [Notebook](https://github.com/minaxixi/Covid-19-Modeling/blob/master/covid_19_EDA.ipynb)
- Visualize the spatial distribution of Covid-19 confirmed cases and deaths on 07-31-2020 in United States via *Plotly*.
- Developed data processing pipeline to process the Covid-19 data via *Spark*.
- Modeled the temporal evolution of Covid-19 confirmed cases via a logistic growth model

## Modeling of Covid-19 Cases with County-Level Demographic and Economic Dataset
- [Notebook](https://github.com/minaxixi/Covid-19-Modeling/blob/master/covid_19_modeling.ipynb)
- Leveraged the county-level demographics and economy data from US Census Bureau.
- Processed the data to join two datasets via a common key and performed data cleaning and missing value imputation.
- Visualized the correlation between features.
- Performed feature selection via LASSO Regression.
- Developed an XGBoost model using selected features to model log10(confirmed_Cases) as a function of county-level demographics and economy information.
- Fine-tuned the model hyperparameters via Randomized Search thru *Scikit-Learn* and achieved an RMSE of 0.15.
- Extracted the feature importance and obtained insight into how the local demographics and economy shape the Covid-19 pandemic spread.
