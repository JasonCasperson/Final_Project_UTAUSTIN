# Project Overview

![Real Estate Market](images/prices-1536x879.jpg)

The real estate market has experienced significant fluctuations between 2021 and 2023. To gain insights into the influence of external factors on home prices, we have conducted an analysis focused on U.S. housing prices on the east coast. This analysis aims to identify potential correlations between housing prices and various features, providing a valuable tool for homebuyers, sellers, and real estate professionals, particularly those interested in the East Coast market.

Our approach involves leveraging data analysis and machine learning techniques, specifically Principal Component Analysis (PCA), K-Means Clustering, regression models, and later, Random Forest. It's important to note that due to the project's two-week timeframe, our analysis primarily focuses on selected zip codes. Therefore, long-term accuracy may vary.

## Tools and Technologies

- Python Pandas
- SQL Database
- Python Matplotlib
- Scikit-learn library

# Data Cleaning

![Data Cleaning](images/61de26cb354ad2f927a95e18_Data%20Cleaning%20Blog%20Images_Blog%20Thumbnail%20Image.png)

The data used for this project was obtained from two primary sources:

1. **USA Real Estate Data**: We sourced this dataset from Kaggle, which includes information about properties such as bedroom count, bathroom count, acreage, city, state, zip code, house size, previous sale date, and price. To maintain the focus on the East Coast, we filtered the dataset to include only East Coast properties.

https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset/data
 
# The Model

![Machine Learning Model](images/61fbec562cf81f62a255f192_61eeb99a54a67e18ce19d47c_0_nyBFE8lLgr8ePAJ_%20(1).jpeg)

Our machine learning approach involves Principal Component Analysis (PCA), clustering, and building a prediction model. The key steps of our model include:

1. **Core Correlation Analysis**: We start by identifying and eliminating outlier correlations to focus on essential correlations.

2. **Data Preprocessing**: The dataset is split into training and testing sets, and the data is standardized for consistency.

3. **PCA and K-Means Clustering**: PCA and K-Means are applied to create data clusters.

4. **Regression Models**: We employ four different regression models, namely Linear Regression, Decision Tree Regressor, Random Forest Regressor, and Gradient Boosting Regressor, to predict housing prices.

5. **Model Evaluation**: The model is cross-validated across the four regression models, and R-squared error analysis is performed to assess correlations.

6. **Feature Importance**: We identify the best-performing model and evaluate the most important features influencing housing prices.

7. **Visualization**: The analysis results are visually presented to the user for easy interpretation.

# Iteration

![Model Iteration](images/mU20bdW.png)

The initial model had some limitations:

- It did not use R-squared error to identify the best correlation grid.
- It lacked an initial correlation check to account for outliers or essential correlations.
- It did not directly access data from the SQL database.
- Initially, Random Forest was not emphasized in the analysis.
- we also tried it with open weather api data but was turned to only real estate data

# Conclusion

![Conclusion](images/ace-attorney-6.webp)

After training and running the data through the model, several conclusions and biases came to light:

- The most prominent features with high correlation to housing prices were house size, zip code, acreage, and the number of bedrooms. Notably, all very common sense conclusions.

- An observable bias was the overrepresentation of addresses from New York, which skewed the analysis results. This bias can be attributed to the concentration of New York data in the dataset.

- A limitation of our analysis was the relatively limited feature set . To conduct more in-depth analysis, further iterations of the model should expand the range of features incorporated.

In conclusion, while our analysis offers valuable insights into factors affecting housing prices with high accuracy of correlation, it's essential to consider the inherent biases and data limitations such as the time and scope of the project. Further research and analysis with more provided features can provide a more comprehensive understanding of housing price dynamics in the East Coast real estate market.
