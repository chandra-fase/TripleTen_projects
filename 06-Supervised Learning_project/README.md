## Project Description

Beta Bank is facing a gradual loss of customers, prompting the realization that retaining existing customers is more cost-effective than acquiring new ones. To mitigate customer attrition, the bank aims to predict whether a customer is likely to leave soon by leveraging historical data on clients' behavior and contract terminations.

Your task is to develop a predictive model with the highest achievable F1 score, indicating the model's precision and recall balance. The minimum threshold for passing this project is an F1 score of at least 0.59, assessed on the test dataset.

The ultimate objective of this project is to develop a robust predictive model that accurately identifies customers at risk of churning from Beta Bank. By achieving a high F1 score and assessing the AUC-ROC metric, the model's effectiveness in identifying potential churners can be evaluated and utilized for proactive customer retention strategies.

## Key Project Objectives:

**Customer Churn Prediction:**
- Utilize historical customer behavior and contract termination data to construct a predictive model that accurately identifies customers likely to churn from Beta Bank.

**Maximizing F1 Score:**
- Emphasize achieving the highest possible F1 score as the primary performance metric for the model. Aim for a balance between precision and recall to accurately predict customer churn.

**Performance Evaluation with Metrics:**
- Assess the model's performance using the F1 score on the test set. Ensure the achieved F1 score meets or exceeds the minimum threshold of 0.59 for project success.
- Measure the Area Under the Receiver Operating Characteristic Curve (AUC-ROC) metric to evaluate the model's overall performance and compare it with the F1 score. This metric provides insight into the model's ability to distinguish between churn and non-churn instances.

## Description of the Data

- `RowNumber` — data string index
- `CustomerId` — unique customer identifier
- `Surname` — surname
- `CreditScore` — credit score
- `Geography` — country of residence
- `Gender` — gender
- `Age` — age
- `Tenure` — period of maturation for a customer’s fixed deposit (years)
- `Balance` — account balance
- `NumOfProducts` — number of banking products used by the customer
- `HasCrCard` — customer has a credit card
- `IsActiveMember` — customer’s activeness
- `EstimatedSalary` — estimated salary
- `Exited` — сustomer has left


## Steps Taken
- Prepared the data by:
  - Renaming columns to follow snake-case rules
  - Removing missing values
  - Changing the `gender` and `geography` columns to int
  - Removing unnecessary columns
- Assigned features and target
- Split the data into train, test and valid
- Scaled numeric data using StandardScaler
- Built and trained the follwing models, providing EDA of the ROC curve:
    <img width="677" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/9c17cd41-c665-4d6e-9643-2b533dc5ea0e">
  - DecisionTreeClassifier
    <img width="701" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/7d1068d5-842f-4a37-b54d-19616dc1fe23">
  - RandomForestClassifier
    <img width="690" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/acc7bbb5-faad-44b6-9b70-8f763d0b1e62">
  - LogisticRegression
    <img width="676" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/208d3e56-7768-4970-ab99-38a5a0407fbd">
- Used upsampling and downsampling to try to fix imbalance issues
- Performed final testing with DecisionTreeClassifier and upsampling since together they produced the best results in training

## General Conclusion

After performing upsampling on the three models our best F1 score was from the DecisionTreeClassification with a score of 0.61 (rounded). With downsampling, our best F1 score was also found with DecisionTreeClassification with a score of 0.59 (rounded). Since our overall best was with the upsampling of the DecsionTreeClassification model, that was the model used in our testing.

After testing the upsampled DecisionTreeModel we achieved a F1 score of 0.59 (rounded). Our recall score is 0.632 and our precision score is 0.548. This means our model is fairly balanced, but is slightly more common to have false positives, and fewer false negatives. With an AUC-ROC score of 0.818, our result is better than the random model as well.

## Suggestions for the Company

**Refinement of DecisionTreeClassification Model:**
- Hyperparameter Tuning: Further optimize the DecisionTreeClassification model by exploring additional hyperparameter tuning techniques. Adjust parameters such as tree depth, minimum samples per leaf, or splitting criteria to potentially enhance the model's predictive performance.
- Ensemble Methods: Experiment with ensemble techniques like Random Forests or Gradient Boosting that utilize multiple decision trees to potentially improve predictive accuracy and generalization.

**Business Outcomes and Customer Retention Strategies:**
- Targeted Customer Retention Efforts: Utilize the model's predictions to identify customers at risk of churning. Develop targeted retention strategies, such as personalized offers, loyalty programs, or proactive customer service initiatives, to prevent churn among high-risk customers.
- Resource Allocation Optimization: Optimize resource allocation by focusing efforts on customers predicted to churn, thereby maximizing the impact of retention initiatives and potentially reducing customer attrition.

**Continuous Model Evaluation and Iteration:**
- Periodic Model Reassessment: Regularly reassess and retrain the model with new data to ensure its continued relevance and accuracy. As customer behavior evolves, updating the model can enhance its predictive power and reliability over time.
- Feedback Loop Integration: Establish a feedback loop by incorporating real-time customer feedback and outcomes of retention strategies back into the model. This loop can enhance model learning and adaptation to changing customer behaviors.

By refining the DecisionTreeClassification model, implementing targeted retention strategies, and continuously evaluating and updating the model, Beta Bank can significantly reduce customer churn rates and enhance customer retention efforts, ultimately leading to improved business outcomes and customer satisfaction.
