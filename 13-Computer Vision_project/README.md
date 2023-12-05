## Project Description

Good Seed, a supermarket chain, aims to leverage data science and computer vision technologies to ensure compliance with alcohol laws by preventing sales to underage individuals. The task involves evaluating the feasibility of using computer vision methods to verify a person's age during alcohol purchases captured by checkout area cameras.

The primary aim of this project is to assess the efficacy of utilizing computer vision algorithms for age verification during alcohol purchases. The findings and conclusions derived from this evaluation will aid Good Seed in making informed decisions regarding the implementation of technology-driven solutions to uphold alcohol sales regulations effectively.

## Key Project Objectives:

**Exploratory Data Analysis (EDA):**
- Conduct a comprehensive exploratory analysis of the dataset containing photographs of individuals with their indicated ages. Gain insights into the distribution of ages, image quality, and potential challenges in age determination.

**Model Training and Evaluation:**
- Utilize computer vision techniques and deep learning algorithms to build a model capable of determining individuals' ages from the provided photographs. Train the model on a GPU-accelerated platform to ensure efficient processing.
Evaluate the model's performance in accurately predicting ages from images, considering metrics such as accuracy, precision, recall, and F1-score.

**Jupyter Notebook Compilation:**
- Compile all code, output, analysis, and findings into a comprehensive Jupyter notebook. Include detailed documentation of the data exploration, model training methodology, evaluation metrics, and visualizations for presentation and future reference.

**Conclusions and Recommendations:**
- Draw conclusive insights from the model evaluation, highlighting its strengths, limitations, and potential areas for improvement.
- Provide actionable recommendations or considerations for implementing a robust age verification system using computer vision in Good Seed supermarkets.

## Description of the Data

- `file_name` - Name of the image
- `real_age` - Age of subject

## Steps Taken
- Cleaned and prepared the dataset by checking for missing values, duplicates and correct datatypes.
- Performed EDA to get an overall impression of the dataset.
  
    <img width="205" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/fafb2f13-c3c8-45e5-9b87-c75a812a75f3">
    
- Trained and evaluated the model by building a 'load_train', a 'load_test', a 'create_model' and a 'train_model' function.
 
    <img width="254" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/b002e1cd-2d7e-4157-bcb8-6bc51e73b292">

- Prepared the script to run on the GPU platform.

## General Conclusion

With our 20 epochs we were able to achieve a MAE of 5.5504, which is great. The system took less than 30 minutes to run, with each epoch taking just over one minute. This could possibly be further improved by adding dropout, and increasing the training time.

## Suggestions for the Company

**Enhanced Model Performance:**
- Dropout Regularization: Implement dropout regularization techniques within the neural network architecture. Dropout can help prevent overfitting and improve the model's generalization, potentially enhancing accuracy and reducing Mean Absolute Error (MAE) further.

**Fine-tuning Training Parameters:**
- Increased Epochs: Consider extending the training duration by increasing the number of epochs beyond 20. Additional epochs could allow the model to converge more accurately, potentially improving its predictive capabilities.
- Hyperparameter Tuning: Experiment with various hyperparameters like learning rate, batch size, or network architecture to optimize the model's performance while maintaining efficient training times.

**Business Outcomes and Implementation:**
- Improved Compliance and Customer Experience: A more accurate age verification system using computer vision can bolster Good Seed's adherence to alcohol laws. This can lead to enhanced compliance, reduced legal risks, and a better shopping experience for customers.

**Operational Efficiency:**
- Scalability and Real-time Implementation: Streamline the model for efficient real-time processing. Optimizing the model's efficiency would enable its deployment across multiple store locations, aiding in prompt age verification during alcohol purchases without hindering checkout speeds.

**Resource Optimization and Cost-effectiveness:**
- Computational Optimization: Continuously seek ways to optimize model training without compromising performance. This could lead to reduced computational resources and training time, potentially resulting in cost savings for implementation and maintenance.

**Feedback Loop and Iterative Improvement:**
- Continuous Model Refinement: Encourage an iterative approach to refine the model based on ongoing evaluations and feedback. Regularly retrain the model with updated data to adapt to evolving customer demographics and improve age prediction accuracy over time.

Implementing these improvements can lead to a more robust and efficient age verification system for Good Seed, contributing to legal compliance, enhanced customer trust, and operational efficiency within their supermarket chain.
