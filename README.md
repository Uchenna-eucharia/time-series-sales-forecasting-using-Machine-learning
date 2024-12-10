# Time-Series Sales Forecasting Using Machine Learning

## Table of Contents
- [Project Description](#project-description)

- [Dataset](#dataset)

- [Tools](#tools)

- [Exploratory Data Analysis](#exploratory-data-analysis)

- [Features](#features)

- [Model Building](#model-building)

- [Model Performance](#model-performance)


### Project Description
This project involves predicting sales for stores and items using time-series forecasting techniques.
The objective is to analyze historical sales data and improve forecasting accuracy through feature enrichment and advanced modeling techniques.


### Dataset
The dataset contains historical sales data with the following columns:

- Date: The date of the sales record.
- Store: Unique identifier for the store.
- Item: Unique identifier for the item.
- Sales: Number of items sold.

### Tools
Programming Language: Python
Libraries Used:
- CatBoost: For model training and prediction.
- Pandas: For data manipulation and analysis.
- Upgini: For feature enrichment.

### Exploratory Data Analysis
- Converted columns to appropriate data types (store and item as strings, date as datetime).
- Chronologically sorted the dataset based on the date column.
- Examined the first few rows to understand the structure and content.

### Features

- Date: Converted to datetime format and used as the primary time-series identifier.
- Store: Categorical variable representing the store.
- Item: Categorical variable representing the item being sold.
- Sales: Numerical target variable representing the number of items sold.
- Enriched Features: Additional features generated using the Upgini library, leveraging the date column for time-series-specific enrichment.

### Model Building
1. Data Splitting:
The dataset was split into training (data before 2017-01-01) and testing (data from 2017-01-01 onward) subsets.

2. Model Selection:
A CatBoostRegressor was selected for its performance on categorical and time-series data.

3. Feature Enrichment:
Leveraged the Upgini library to add new features to the dataset using the date column as a search key.

4. Training and Prediction:
The model was trained on both the original dataset and the enriched dataset.

### Model Performance

1. Before Feature Enrichment: The model achieved a SMAPE of 39.56%, indicating that predictions deviated significantly from actual sales values when using the original dataset.

2. After Feature Enrichment: With enriched features, the SMAPE improved to 15.99%, showing a substantial reduction in prediction error and enhanced forecasting accuracy.

3. Key Improvement: Feature enrichment reduced the prediction error by over 23 percentage points, demonstrating the value of additional contextual features in improving model performance.

