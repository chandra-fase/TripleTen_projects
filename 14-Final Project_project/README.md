## Project Description

Interconnect, a telecom operator, seeks to predict customer churn to proactively retain clients. By identifying customers likely to leave, they aim to offer targeted incentives and special plans to mitigate churn. The marketing team has gathered client data encompassing plan details, contracts, and personal information.

The primary objective is to develop a predictive model capable of anticipating customer churn for Interconnect. By leveraging data analysis and machine learning techniques, the project aims to empower the marketing team with insights to implement proactive measures and retain customers effectively.

## Key Project Objectives:

**Data Analysis and Exploration:**
- Conduct comprehensive data analysis to understand the patterns, trends, and factors influencing customer churn. Explore features related to plans, contracts, and customer demographics to identify potential indicators of churn.

**Data Preprocessing and Feature Engineering:**
- Cleanse the dataset by handling missing values, outliers, and inconsistencies. Create new features or transform existing ones to extract valuable insights. This may involve feature scaling, encoding categorical variables, or creating aggregated metrics.

**Model Development and Hyperparameter Tuning:**
- Build multiple predictive models using machine learning algorithms such as logistic regression, decision trees, random forests, or gradient boosting. Implement hyperparameter tuning techniques like cross-validation to optimize model performance.

**Evaluation and Model Selection:**
- Evaluate the trained models using appropriate metrics like accuracy, precision, recall, or F1-score to assess their predictive capability for identifying potential churners.

**Business Insights and Recommendations:**
- Derive actionable insights from the model results, highlighting influential features and their impact on churn prediction. Provide recommendations for tailored retention strategies based on the model's predictions.

## Description of the Data

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

## Steps Taken
**Work Plan**
- Checked the datasets for missing and duplicate values, and changing data types when necessary.
- Performed exploratory data analysis to figure out which questions needed to be asked for the work plan. This included:
  - Merging the four data frames.
  - Creating a target feature.
  - Removing outliers.
  - Visualizing the distribution of monthly charges between churned and not churned customers, as well as the distribution of monthly charges by gender and churned status and senior citizens and their churned status.
 
    <img width="223" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/ba045fd6-77fc-4a55-8725-82d8911c70a9">

    <img width="269" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/547b1ef1-dc74-4413-af24-c4a50d43cc71">

- Used results of EDA to complete a work plan including, clarifying questions, and next steps.

**Solution Code**
-  Missing values in `TotalCharges` were imputed using SimpleImputer and missing values for `MultipleLines` and various Internet services after merging the datasets were replaced with "No", since this meant the customer did not opt for these services.
-  Created `num_day` derived by taking the difference between `EndDate` and `BeginDate` as well as creating `num_pmt` which is a ratio of `TotalCharges`/`MonthlyCharges`.
- Stratfied and split the dataset into train and test into a ratio of 80:20.
  - A copy of this dataset was also created, to test whether `num_days` caused any leakage
- Applied Ordinal Encoding for the Type and PaymentMethod features.
  - Scaled the numerical features such as `num_days`, `num_pmt`, `num_services`, `MonthlyCharges`, and `TotalCharges`, including the date features.
  - One-hot encoded the boolean features.
- Built six models using LogisticRegression, RandomForestClassifier and CatBoostClassifier. Each model was trained on the two datasets.

    <img width="501" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/dbfe091a-28a3-454e-bdd9-d4db9cb5c6e9">

    <img width="311" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/b01492af-f151-4fcc-9c18-199dfe6349df">

  - Used 5-fold cross validation during GridSearch to identify useful hyperparameters for the respective models. Only one or two hyperparameters were tuned to save time.

## General Conclusion

- The following customer features were engineered:
  - `num_days` - dervied by taking the difference between `EndDate` and `BeginDate`
  - `num_pmt` - derived by taking the ratio between 'TotalCharges' and `MonthlyCharges`
  - `num_services` - counts a yes for either phone service or internet related service as a 1 or 0, then it is totaled to determine the number of services a customer has signed up for
- Missing values in the phone and internet related features were replaced with 'No' as these represent customers who did not have these services.
- Numerical features such as `MonthlyCharges`, `num_days`, `num_pmt`, `num_service` and `TotalCharges` were scaled on the training set. Similarly, the categorical features and binary features where encoded using one-hot encoding.
- Redundant features such as `CustomerId`, `BeginDate`, and `EndDate` were dropped and four models were built.
- Upsampling didn't help with improving the AUC ROC score. However, increasing the train test ratio from 80:20 to 90:10 did help the model improve by 1%.
- 5-fold CV with Gridsearch was used to identify the suitable hyperparameters for the respective models. For example, in LogisticRegression C was tuned. For RandomForest, it was n_estimators and max_depth. Iterations was tuned for CatBoost.
- The best model in terms of ROC-AUC and time to train the model is LogisticRegression with a AUC of 91% on the test set and a training time of less than 7 seconds.
  - The marketing team of the telco can use this model to identify churn. In addition, they can improve the signal by adding features around usage of various plans, location of customer, customer complaints, time to resolve them, etc.

## Suggestions for the Company

**Enhancement of Predictive Features:**
- Incorporate Usage Patterns: Include features related to usage behaviors such as call duration, data usage, plan changes, or frequency of service usage. These insights can provide a deeper understanding of customer behavior and enhance predictive accuracy.

**Customer Experience and Service Improvement:**
- Integrate Customer Feedback Data: Incorporate data on customer complaints, satisfaction ratings, or resolution time into the model. Analyzing these factors could highlight areas requiring service improvement, leading to better customer retention strategies.

**Localized Strategies and Customer Segmentation:**
- Regional Analysis: Explore regional data to identify geographic-specific churn patterns. Tailor retention strategies based on region-specific trends, addressing localized customer needs more effectively.

**Continuous Model Refinement:**
- Regular Model Updates: Periodically retrain the model with new data to account for evolving customer behavior and trends. Continuous model refinement can ensure that the model remains effective over time.

**Personalized Offerings and Retention Plans:**
- Targeted Promotions: Utilize the predictive model to craft personalized retention offers for customers identified as potential churners. Implement targeted promotions or special plans to incentivize these customers to stay.

**Cross-functional Collaboration:**
- Collaboration with Service Teams: Encourage collaboration between the data science team and customer service teams. Insights from the model can guide service improvements and customer interactions to reduce churn rates.

**Ethical Considerations and Customer Privacy:**
- Ethical Compliance: Ensure adherence to data privacy laws and ethical considerations while using customer data. Maintain transparency and safeguard customer privacy throughout the data analysis and retention strategy implementation.

Implementing these suggestions can facilitate better retention strategies, improved customer satisfaction, and ultimately reduce churn rates for the telecom operator. The integration of additional relevant features and continuous model updates will enable the company to stay proactive in addressing customer churn effectively.
