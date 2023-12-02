## Project Description

Sweet Lift Taxi company aims to optimize driver availability during peak hours at airports by accurately forecasting the volume of taxi orders for the upcoming hour. Leveraging historical taxi order data, the project goal is to construct a predictive model capable of forecasting order volumes with high accuracy.

The project's primary objective is to develop an accurate predictive model to anticipate taxi order volumes, aiding Sweet Lift Taxi company in efficiently managing driver availability during peak hours. By leveraging predictive analytics, the company aims to enhance operational efficiency and better meet customer demands, ultimately optimizing service quality.

## Key Project Steps:

**Data Collection and Resampling:**
- Download historical taxi order data and resample it on an hourly basis to create a time series dataset aligned with hourly intervals.

**Data Analysis:**
- Conduct exploratory data analysis (EDA) to gain insights into the patterns, trends, and seasonality within the taxi order data. Identify key features and potential relationships that might influence order volumes during different hours.

**Model Training with Hyperparameter Variations:**
-Train diverse models with different hyperparameters, including time series models (e.g., ARIMA, SARIMA), regression-based models (e.g., Linear Regression), and ensemble methods (e.g., Random Forest, Gradient Boosting). Experiment with various configurations to determine the most accurate predictive model.

**Test Set Evaluation and Conclusion:**
- Reserve 10% of the initial dataset as a test sample to evaluate model performance. Measure the Root Mean Squared Error (RMSE) on the test set for each model to ensure it does not exceed 48.
- Draw conclusions based on model performance, identifying the model(s) that best forecast taxi order volumes for the next hour.

## Description of the Data

- `num_orders` - Number of orders
- `datetime` - Date of ride

## General Conclusion

- The mean 'num_orders' shows an upward trend in the last 5 months between March 1, 2018 and August 31, 2018.
- The data was prepared by creating several date and time-series related features, such as, `month`, `day`, `dayofweek`, `hour`, `lag_*`, `rolling_mean`, `rolling_median`, and `rolling_std`.
- The decomposition of time-series components shows a daily seasonality, which peaks at 12 AM, and drops to its lowest at 6AM, and during the day peaks at around 5PM.
- RandomForestRegressor emerged as the best model with the lowest RMSE. However, it also took the longest to train the model.

## Suggestions for the Company

**Model Optimization for Improved Training Time:**
- Feature Selection: Assess feature importance and reduce the feature set to the most influential variables. This can streamline the model training process by focusing on key predictors, potentially reducing the training time.
- Model Compression Techniques: Explore techniques like model compression or dimensionality reduction (e.g., PCA) to simplify the model complexity without compromising prediction accuracy. This can lead to faster training times while maintaining performance.

**Operational Improvements and Business Outcomes:**
- Resource Allocation Optimization: By reducing model training time without compromising accuracy, Sweet Lift Taxi can optimize computational resources, allowing quicker updates and retraining of models to adapt to changing demand patterns.
- Service Planning and Customer Satisfaction: Accurate predictions assist in better scheduling and deployment of drivers during peak hours, leading to improved service reliability and customer satisfaction, potentially attracting more customers.

**Continuous Model Evaluation and Deployment:**
- Regular Model Updates: Continuously evaluate and update the model with new data to maintain relevance and accuracy. Regular model recalibration ensures alignment with changing trends and patterns in taxi orders.
- Real-time Prediction Implementation: Deploy optimized models in a real-time environment to provide instant forecasts, enabling proactive decision-making in managing driver availability.

By optimizing model training time while maintaining prediction accuracy, Sweet Lift Taxi can streamline operations, enhance service quality, and adapt efficiently to dynamic demand patterns, ultimately providing a more reliable and customer-centric taxi service.
