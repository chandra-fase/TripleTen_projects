## Project description

The telecom operator Interconnect would like to be able to forecast their churn of clients. If it's discovered that a user is planning to leave, they will be offered promotional codes and special plan options. Interconnect's marketing team has collected some of their clientele's personal data, including information about their plans and contracts.

## Description of the data

- `customerID` - Unique ID
- `gender` - Gender
- `SeniorCitizen` - Whether senior citizen or not
- `Partner` - Has partner or not
- `Dependents` - Number of dependents
- `BeginDate` - Joining date
- `EndDate` - Ending date
- `Type` - Plan type
- `PaperlessBilling` - Type of paperpless billing
- `PaymentMethod` - Payment method
- `MonthlyCharges` - Monthly charges
- `TotalCharges` - Total charges
- `MultipleLines` - Whether has multiple lines
- `InternetService` - Whether has internet service
- `OnlineSecurity` - Whether has online security
- `OnlineBackup` - Whether has online backup
- `DeviceProtection` - Whether has device protection
- `TechSupport` - Whether has tech support
- `StreamingTV` - Whether has streaming TV
- `StreamingMovies` - Whether has streaming movies
- `is_churned` - Whether churned
- `num_days` - Number of days in the system
- `year` - Year
- `num_services` - Number of services availed

## Answer these questions:

- Perform data analysis.
- Create new features and clean the data.
- Build different models and perform hyperparameter tuning with cross validation

## General conclusion

- The following customer features were engineered:
  - `num_days` - dervied by taking the difference between `EndDate` and `BeginDate`
  - `num_pmt` - derived by taking the ratio between 'TotalCharges' and `MonthlyCharges`
  - `num_services` - counts a yes for either phone service or internet related service as a 1 or 0, then it is totalled to determine the number of services a customer has signed up for
- Missing values in the phone and internet related features were replaced with 'No' as these represent customers who did not have these services.
- Numerical features such as `MonthlyCharges`, `num_days`, `num_pmt`, `num_service` and `TotalCharges` were scaled on the training set. Similarly, the categorical features and binary features where encoded using one-hot encoding.
- Redundant features such as `CustomerId`, `BeginDate`, and `EndDate` were dropped and four models were built.
- Upsampling didn't help with improving the AUC ROC score. However, increasing the train test ratio from 80:20 to 90:10 did help the model improve by 1%.
- 5-fold CV with Gridsearch was used to identify the suitable hyperparameters for the respective models. For example, in LogisticRegression C was tuned. For RandomForest, it was n_estimators and max_depth. Iterations was tuned for CatBoost.
- The best model in terms of ROC-AUC and time to train the model is LogisticRegression with a AUC of 91% on the test set and a training time of less than 7 seconds.
  - The marketing team of the telco can use this model to identify churn. In addition, they can improve the signal by adding features around usage of various plans, location of customer, customer complaints, time to resolve them, etc.
