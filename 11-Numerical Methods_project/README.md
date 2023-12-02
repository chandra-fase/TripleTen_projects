## Project Description

Rusty Bargain, a used car sales service, aims to develop a user-friendly app enabling customers to swiftly determine their car's market value. Leveraging historical data encompassing technical specifications, trim versions, and prices, the goal is to construct an accurate and efficient predictive model for assessing car values.

The project's primary focus is to build and evaluate predictive models for determining car market values, emphasizing model accuracy while considering computational efficiency for efficient app functionality. By comparing various algorithms and assessing their performance across key evaluation criteria, Rusty Bargain aims to deploy a robust and responsive app, delivering accurate car value predictions swiftly to its users.

## Key Objectives:

**Model Development for Market Value Prediction:**
- Develop a predictive model to estimate the market value of cars based on historical data. Focus on model accuracy, speed, and training time as primary evaluation criteria.

**Model Comparison with Various Algorithms:**
- Train multiple models with diverse hyperparameters, including Random Forest, Decision Tree, Linear Regression, and different implementations of Gradient Boosting techniques (excluding similar Gradient Boosting variants). This comparison aims to assess the predictive quality and computational efficiency of these models.

**Performance Evaluation Metrics:**
- Assess and compare models based on predictive accuracy, measured by metrics such as Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), or R-squared (R2). Additionally, evaluate the speed of predictions and the duration required for model training to determine computational efficiency.

**Analysis and Comparative Study:**
- Analyze the trade-offs between model accuracy, speed of prediction, and training time for each model. Identify which models offer the best balance between accurate market value predictions and computational efficiency.

## Description of the Data

- `DateCrawled` — date profile was downloaded from the database
- `VehicleType` — vehicle body type
- `RegistrationYear` — vehicle registration year
- `Gearbox` — gearbox type
- `Power` — power (hp)
- `Model` — vehicle model
- `Mileage` — mileage (measured in km due to dataset's regional specifics)
- `RegistrationMonth` — vehicle registration month
- `FuelType` — fuel type
- `Brand` — vehicle brand
- `NotRepaired` — vehicle repaired or not
- `DateCreated` — date of profile creation
- `NumberOfPictures` — number of vehicle pictures
- `PostalCode` — postal code of profile owner (user)
- `LastSeen` — date of the last activity of the user
- `Price` — price (Euro)

## General Conclusion

- RustyBargain will have to make a compromise between a 24x increase in training time versus a +/- 1.1x increase in RMSE should it decide between the top 2 models - RandomForestRegression and CatBoostRegression.
- However, CatBoostRegressor offers several hyperparameters to play with, and increasing the number of iterations, and adding regularization may help in achieving a better RMSE. Therefore, in my view, they should pick CatBoostRegression simply because it is really fast, and it offers several options to improve the evaluation metric.

## Suggestions for the Company

**Hyperparameter Tuning and Optimization:**
- CatBoostRegressor Hyperparameters: Conduct a thorough hyperparameter tuning process for CatBoostRegressor, exploring various configurations. Adjusting parameters like the number of iterations, depth of trees, learning rates, and regularization might significantly enhance the model's predictive accuracy while balancing training time.

**Feature Engineering and Selection:**
- Additional Feature Exploration: Explore additional relevant features or derive new ones from the existing dataset. Features capturing nuanced details about the cars' conditions, historical trends, or market fluctuations might enhance the model's predictive power.

**Business Outcomes:**
- Enhanced Customer Experience: Improved accuracy in predicting car market values can significantly enhance customer satisfaction by providing more precise and reliable estimates. This can lead to increased user engagement and retention within RustyBargain's app.
- Competitive Advantage: A highly accurate and fast app for estimating car values can set RustyBargain apart from competitors, attracting more users and increasing the app's popularity and market share.

**Continuous Model Refinement:**
- Continuous Monitoring and Updating: Continuously monitor model performance and retrain the model periodically with updated data. Regular updates ensure that the model stays relevant and maintains accuracy over time as market dynamics change.

**Operational Efficiency:**
- Resource Allocation Optimization: By deploying an efficient model like CatBoostRegressor, RustyBargain can optimize computational resources and reduce costs associated with model training and inference, enhancing operational efficiency.

By fine-tuning hyperparameters, continuously updating the model, and leveraging its improved accuracy for customer satisfaction, RustyBargain can enhance its app's effectiveness and maintain a competitive edge in the used car sales market.
