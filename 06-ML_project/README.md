## Project Description

Megaline, a mobile carrier, aims to modernize subscribers' plans by transitioning them from legacy plans to newer offerings: Smart or Ultra. Leveraging behavior data from subscribers who have successfully switched plans, this project focuses on developing a robust model for recommending the appropriate plan to existing subscribers.

Your role involves building a classification model that accurately predicts and recommends either the Smart or Ultra plan based on subscribers' behavior patterns. The data preprocessing step has been completed, allowing direct progression to model creation.

**Key Project Objectives:**

- Model Development for Plan Recommendation:
  - Utilize the preprocessed behavior data to construct a classification model that accurately predicts the suitable plan (Smart or Ultra) for subscribers. The primary goal is to achieve the highest possible accuracy in plan recommendations.
- Accuracy Threshold and Model Evaluation:
  - The project's success criterion is an accuracy threshold of 0.75. Verify the model's accuracy using a separate test dataset to ensure its reliability in predicting plan recommendations for subscribers who have not yet switched plans.
- Optimizing Model Performance:
  - Employ various machine learning algorithms and techniques to develop a high-performing model. Experiment with hyperparameter tuning, feature selection, or ensemble methods to maximize the model's accuracy.

The ultimate objective of this project is to create a robust classification model that can accurately predict the appropriate plan—Smart or Ultra—for Megaline's subscribers based on their behavior data. Achieving an accuracy threshold of 0.75 or higher ensures the model's efficacy in facilitating plan transitions and enhancing subscribers' experiences with Megaline's updated offerings.

## Description of the Data

Every observation in the dataset contains monthly behavior information about one user. The information given is as follows:
- `сalls` — number of calls,
- `minutes` — total call duration in minutes,
- `messages` — number of text messages,
- `mb_used` — Internet traffic used in MB,
- `is_ultra` — plan for the current month (Ultra - 1, Smart - 0).


## Answer These Questions:

- Split the source data into a training set, a validation set, and a test set.
- Investigate the quality of different models by changing hyperparameters. Briefly describe the findings of the study.
- Check the quality of the model using the test set.
- Additional task: sanity check the model. This data is more complex than what you’re used to working with, so it's not an easy task. We'll take a closer look at it later.


## General Conclusion

Using DummyClassifier to random guess gives us an accuracy close to 70%. Lower than all other ML models tested. The highest accuracy comes from the RandomForestClassifier model with n_estimators = 5. The lowest accuracy was seen as a result of using LogisticRegression, which was just slightly above the random guess.

## Suggestions for the Company

**Model Selection and Refinement:**
- Optimizing RandomForestClassifier: Given its highest accuracy among the tested models, focus on further optimizing the RandomForestClassifier with n_estimators = 5. Explore adjusting hyperparameters, such as increasing the number of estimators or fine-tuning other parameters, to potentially improve accuracy.
- Refining LogisticRegression: Despite its lower accuracy, delve deeper into LogisticRegression's performance. Investigate feature importance, data balance, or regularization techniques to enhance its predictive capabilities. Sometimes, simpler models like LogisticRegression might be advantageous due to their interpretability and efficiency.

**Feature Engineering and Selection:**
- Feature Importance Analysis: Conduct a comprehensive analysis of feature importance within the RandomForestClassifier model. Identify and prioritize the most influential features impacting plan recommendations. Streamline features or engineer new ones that might enhance predictive accuracy.

**Business Outcomes and Customer Experience:**
- Enhanced Plan Transition Strategies: A more accurate model for plan recommendations can lead to better subscriber experiences. Accurately suggesting the most suitable plan (Smart or Ultra) based on subscriber behavior can potentially increase customer satisfaction and loyalty.
- Optimized Marketing and Communication: Utilize the model to tailor marketing campaigns or personalized offers, providing targeted promotions for subscribers based on the predicted plan recommendations. This can increase engagement and conversion rates among legacy plan users.

By refining existing models, optimizing feature engineering, and leveraging the model for personalized marketing strategies, Megaline can enhance plan transition accuracy and subscriber satisfaction, ultimately leading to improved customer retention and business growth.
