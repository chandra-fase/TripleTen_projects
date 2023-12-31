## Project Description

Sure Tomorrow insurance company seeks to leverage Machine Learning to address various challenges within their operations, aiming to optimize marketing strategies, improve risk assessment, and safeguard client privacy.

The project aims to harness Machine Learning capabilities to enhance marketing strategies, optimize risk assessment, and ensure client privacy for Sure Tomorrow insurance company. By leveraging predictive models and privacy protection measures, the company endeavors to improve decision-making while prioritizing data privacy and security for its customers.

## Key Tasks

**Customer Similarity Identification:**
- Identify customers similar to a reference customer to aid the company's agents in targeted marketing efforts. Utilize Machine Learning techniques to cluster customers based on similarities in preferences, behavior, or demographics.

**Insurance Benefit Prediction for New Customers:**
- Develop a predictive model to forecast whether a new customer is likely to receive insurance benefits. Compare the model's performance against a baseline (dummy model) to assess predictive accuracy and potential improvements.

**Prediction of Insurance Benefit Quantity:**
- Construct a linear regression model to predict the count or quantity of insurance benefits a new customer is expected to receive. Utilize historical data and relevant features to create an accurate prediction model.

**Privacy Preservation in Model Deployment:**
- Ensure the protection of clients' personal data while deploying the predictive model from the previous task. Implement privacy-preserving techniques or anonymization strategies to safeguard sensitive information without compromising model performance.

## Description of the Data

- `gender` - Gender
- `age` - Age of insured
- `salary` - Salary of insured
- `number of family members` - Number of dependents

## Steps Taken
- Cleaned and preprocessed the data by removing duplicate values, as well correcting column data types.
- Performed EDA to visualize if any obvious customer groups exist.

    <img width="312" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/c5bb38b1-a5ed-4029-bc38-bedbf5428484">
    
- Created a function to return k nearest neighbors for the nth object based on a specified distance.
    <img width="490" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/072ce9af-a248-4b14-970e-ae42d3d89c5e">
- Tested the function for four combinations of two case:
  - Scaling:
    - The data is not scaled
    - The data is scaled with the MaxAbsScaler
  - Distance Metrics
    - Euclidean
    - Manhattan
- Built a KNN-based classifier and measured its quality with the F1 metric for k = 1...10 for both the original data and the scaled data.

    <img width="290" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/1d457760-d555-420c-8340-27850b1a991b">
- Created a dummy model to test it with four different probability values:
  - 0
  - Probability of paying any insurance benefit
  - 0.5
  - 1
- Obfuscated the data by multiplying the numerical features by an invertible matrix *P*. 

## General Conclusion

- We used KNearestNeighbhors to find the customer closest to a given customer; the solution was improved with scaling the data, and using the Euclidean metric to improve the predictions.
- We also built models to help the marketing team predict whether a customer will likely receive insurance benefits or not. And, the resulting model with scaled data, performed very well compared to a dummy model. The resulting model produced had an F1 score of 92% on the validation set.
- We built a LinearRegression model on both scaled and unscaled data, to predict the number of insurance benefits a new customer would receive; the model produced a moderately high R2 score 66%. What we have observed is that scaling didn't impact the results.
- We obfuscated the data, and showed analytically that there is no difference between the obfuscated data and the original data.
- We also proved this computationally, by building a LinearRegression model using the obfuscated data, and the resulting RMSE and R2 scores were identical to that obtained with modeling the original data.

## Suggestions for the Company

**Enhancing Predictive Models:**
- Feature Engineering: Explore additional features or derive new ones to improve the predictive power of models. Features related to customer interactions, historical insurance claims, or external data sources could enhance predictions.

**Fine-Tuning Regression Models:**
- Feature Scaling Exploration: Revisit the impact of scaling on the Linear Regression model's performance. Experiment with different scaling methods or feature transformations to ascertain potential improvements in predicting insurance benefit quantities.

**Continuous Model Validation and Iteration:**
- Model Performance Monitoring: Continuously monitor model performance with new data and refine models iteratively. Regular retraining with updated data ensures model relevance and accuracy over time.
- Adaptive Privacy Measures: Adapt privacy-preserving strategies as per evolving data privacy regulations to maintain compliance and uphold data security standards.

By refining predictive models, and continuously iterating on model performance, Sure Tomorrow can strengthen its predictive capabilities, protect client data, and drive improved business outcomes, leading to more effective decision-making and enhanced customer satisfaction.
