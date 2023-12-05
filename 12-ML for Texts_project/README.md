## Project Description

The Film Junky Union, a vibrant community dedicated to classic movie enthusiasts, is developing an automated system to categorize and filter movie reviews. The primary objective is to create a model capable of identifying negative reviews within IMBD movie reviews, aiming for an F1 score of at least 0.85 to ensure robust performance.

The project aims to develop a robust model capable of automatically detecting negative movie reviews within the IMBD dataset. By leveraging machine learning algorithms and thorough analysis, the Film Junky Union aims to enhance their review categorization system, catering to their community's preferences and needs.

## Key Project Steps:

**Exploratory Data Analysis (EDA):**
- Perform an in-depth exploration of the IMBD movie review dataset, analyzing the distribution of positive and negative reviews to understand class imbalances and potential biases.

**Data Preprocessing:**
- Prepare and preprocess the dataset for modeling, including text cleaning, handling missing values, tokenization, and converting text into numerical representations suitable for model training.

**Model Training:**
- Train a minimum of three distinct models using the provided training dataset. Experiment with various algorithms to classify positive and negative reviews accurately.

**Model Testing and Evaluation:**
- Test the trained models using a separate test dataset, measuring their performance metrics such as accuracy, precision, recall, and F1 score to assess their ability to classify negative reviews effectively.

**Personal Review Classification:**
- Craft sample movie reviews and utilize the trained models to classify them as either positive or negative. Compare the models' classifications on these self-generated reviews.

**Analysis of Model Discrepancies:**
- Analyze and explain differences observed in the testing results between the models when classifying the provided test dataset and the self-generated movie reviews.

**Findings Presentation:**
- Compile and present comprehensive findings, including insights from the EDA, model performances, discrepancies in classification results, and recommendations for model improvement or selection based on the project's objectives.

## Description of the Data

- `review`: the review text
- `pos: the target`, '0' for negative and '1' for positive
- `ds_part`: 'train'/'test' for the train/test part of dataset, correspondingly

## Steps Taken
- Cleaned and prepared the dataset by checking for missing values, duplicates and correct datatypes.
- Used EDA to visualize the number of reviews of the years and the distribution of number of reviews per movie with the exact counting and KDE.
  
    <img width="482" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/d2e49306-6fdb-44e4-8593-2e554b87ce0f">
<img width="487" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/6fd73098-8456-4899-86ff-0a05d028648b">

- EDA was also used to visualize any imbalance between the train and test datasets.
    <img width="483" alt="image" src="https://github.com/chandra-fase/TripleTen_projects/assets/132231330/cabd6034-4c12-440d-80f1-d824d3d0f878">
- Composed an evaluation function to be used for all models.
- Cleaned up the review texts using WordNetLemmatizer.
- Trained and tested three different models:
  - NLTK, TF-IDF and LogisticRegression
  - spaCy, TF-IDF and LogisticRegression
  - spaCy, TF-IDF and LGBMClassifier
- Classified a few provided reviews with all of the models.
- Checked for differences between the testing results of models.

## General Conclusion

- The DummyClassifier, as expected, produces an F1 score of 50%, which is as good as flipping an unbiased coin.
- Comparing the LogisticRegression models with NLTK used for preprocessing and Spacy for preprocessing, the model with reviews preprocessed using NLTK, comes out at the top with best f1 score of 88%.
- Both the models were trained using 5 fold cross-validation with hyperparameter tuning on the C parameter.
- The LightGBM model turned out to have a lower f1 score, and it took more than two hours to complete training.

## Suggestions for the Company

**Advanced Text Preprocessing Techniques:**
- NLP Libraries Exploration: Explore and experiment with different natural language processing (NLP) libraries beyond NLTK and Spacy. Consider other libraries or techniques for text preprocessing, like stemming, lemmatization, or feature engineering, to enhance model performance further.

**Hyperparameter Optimization and Model Selection:**
- Fine-tuning Hyperparameters: Conduct a more exhaustive hyperparameter search for the models. Explore a wider range of hyperparameters or ensemble techniques for the LightGBM model to potentially enhance its performance while optimizing training time.
- Model Selection Strategy: Experiment with different algorithms beyond those explored in this project. Try gradient boosting variants or deep learning approaches to ascertain if they offer improved F1 scores without significantly increasing training time.

**Business Outcomes and User Experience:**
- Enhanced Review Categorization System: Implementing an accurate model with high F1 scores can significantly improve the Film Junky Union's review categorization system. This could enhance user experience by offering better-filtered content, attracting more users to the community.

**Operational Efficiency:**
- Optimized Model Training Time: Streamline model training processes to reduce training time, potentially using more efficient algorithms or optimized hyperparameters. This would lead to quicker model updates, ensuring relevance with the latest reviews.

**Community Engagement and Retention:**
- Improved Recommendations: Accurate identification of negative reviews can aid in tailoring movie recommendations, increasing user engagement, and potentially retaining more members within the Film Junky Union community.

Implementing these enhancements could lead to a more accurate and efficient review categorization system for the Film Junky Union, driving better user experiences and community engagement while optimizing operational efficiency.
