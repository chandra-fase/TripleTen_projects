## Project Description

The data is stored in three files:

- gold_recovery_train.csv — training dataset download
- gold_recovery_test.csv — test dataset download
- gold_recovery_full.csv — source dataset download

The project entails data analysis and modeling within the mining industry, utilizing a dataset consisting of training and test sets containing various parameters indexed by acquisition date and time. The primary objectives are to ensure data correctness, perform comprehensive data preprocessing, and build a predictive model to forecast recovery rates in the extraction process.

## Key Project Steps:

**Data Correctness Verification:**
- Validate the correctness of recovery calculations using the training set. Compute Mean Absolute Error (MAE) between calculated and provided rougher output recovery values. Document findings to assess the accuracy of the recovery feature.

**Feature Analysis and Preprocessing:**
- Identify and analyze features absent in the test set. Determine the types of these parameters to understand their significance and potential impact on model building.
- Perform data preprocessing tasks, including handling missing values, encoding categorical variables, and scaling numerical features for optimal model performance.

**Metal Concentration Analysis:**
- Investigate the changes in gold (Au), silver (Ag), and lead (Pb) concentrations across purification stages. Document trends and variations in concentrations to understand their evolution through the extraction process.

**Particle Size Distribution Comparison:**
- Compare feed particle size distributions between the training and test sets. Evaluate the significance of any observed variations, ensuring consistency for accurate model evaluation.

**Total Substance Concentration Examination:**
- Assess total substance concentrations at different extraction stages (raw feed, rougher concentrate, and final concentrate). Identify and address any abnormal values that might skew the distribution, considering their removal for data integrity.

**Performance Metric Function and Model Training:**
- Develop a function to calculate the final symmetric Mean Absolute Percentage Error (sMAPE) value for model evaluation.
- Train various models using cross-validation techniques to predict recovery rates. Evaluate model performance and select the best-performing model for testing using the test sample.

The project aims to ensure data accuracy, perform comprehensive preprocessing, and construct a robust predictive model to forecast recovery rates in the mining extraction process. By addressing anomalies, understanding parameter significance, and selecting an optimal model, the project endeavors to improve forecasting accuracy in the mining industry's extraction operations.

## Description of the Data

- `rougher.output.recovery`  - Output of the rougher
- `rougher.output.tail_ag`   - Concentration of Silver
- `rougher.output.tail_sol`  - Concentration of solution
- `rougher.output.tail_au`   - Concentration of Gold
- `rougher.input.floatbank11_xanthate` - Floatation bank input
- `secondary_cleaner.output.tail_sol`  - Secondary stage cleaner concentrate
- `final.output.recovery`  - Final output
- `rougher.calculation.au_pb_ratio`  - Gold to Lead ratio
- `primary_cleaner.input.sulfate`   - Concentrate of sulphate
- `primary_cleaner.input.depressant` - Concentrate of depressant

## Steps Taken
- Opened and looked over datasets.
- Checked that recovery was calculated correctly by using the training set to calculate recovery for the `rougher.output.recovery` features and finding the mean absolute error (MAE) between the calculations and the feature values.
- Performed data preprocessing by merging datasets and dealing with missing values.
- Used EDA to compare feed particle size distributions in the training set and in the test set.
    <img width="488" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/8ab3f7d3-c9b3-4c59-885a-e2156e9e35bf">
    <img width="359" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/f06508e4-5da3-4740-ab7f-c9e3402ae52d">
- Also, created graphs to visualize total concentration of all metals at certain stages.
    <img width="476" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/9434f79f-142f-4ce7-be95-bc5ab3ea5b5f">
- Created a function to calculate the final sMAPE value.

    <img width="340" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/e7ebc781-35d6-4936-855e-147e2137cca3">
- Trained the following models and evaluated them using cross-validation:
  - LinearRegression
  - DecisionTreeRegressor
  - RandomForestRegressor
- Chose the best model (RandomForestRegressor) and tested it using the test sample.

## General Conclusion

We compared several models with Dummy Regressor (sMAPE=0.1029):
- Linear regression: 0.1238
- Decision tree regressor: nan
- Random forest regressor: 0.1177 with a 0.1047 score on the test set with 66% accuracy.

It seems that the Dummy Regressor has the best result according to the sMAPE

## Suggestions for the Company

**Refinement of Model Selection:**
- Hyperparameter Tuning: Revisit the models with poor performance, such as the Decision Tree Regressor, to perform hyperparameter tuning. Adjust parameters like tree depth, minimum samples per leaf, or splitting criteria to improve their predictive capability.

**Feature Engineering and Selection:**
- Advanced Features: Consider engineering new features or incorporating additional domain-specific knowledge to enhance model performance. Features related to mineral characteristics, extraction processes, or temporal patterns might improve predictions.
- Feature Importance: Evaluate feature importance across models to identify influential variables. Focus on relevant features that significantly impact recovery rate predictions.

**Data Quality and Anomaly Handling:**
- Anomaly Detection: Revisit data cleaning and anomaly handling procedures to ensure data quality. Investigate any outliers or anomalies in the dataset that might be adversely affecting model performance and rectify or remove them appropriately.

**Business Outcomes:**
- Operational Efficiency: Improved recovery rate predictions can optimize operational efficiency in the extraction process. Accurate forecasts assist in resource allocation, ensuring optimal use of mining equipment, personnel, and resources.
- Cost Reduction and Profit Maximization: Precise recovery rate predictions can minimize unnecessary costs and maximize profits by reducing waste and optimizing extraction strategies based on accurate forecasts.

**Continuous Model Evaluation and Deployment:**
- Regular Model Reassessment: Continuously reassess model performance with new data to ensure its relevance and accuracy over time. This continuous evaluation enables the identification of model drift or changing patterns in the extraction process.
- Scalable Deployment: Prepare the best-performing model for deployment in real-time operational systems. Ensure the model's scalability and efficiency in processing new data for ongoing predictive analysis in mining operations.

By refining model selection, improving feature engineering, addressing data quality issues, and leveraging accurate recovery rate predictions, the mining industry can optimize operations, reduce costs, and enhance profitability through efficient resource utilization and informed decision-making.
