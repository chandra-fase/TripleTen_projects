## Project description

The Film Junky Union, a new edgy community for classic movie enthusiasts, is developing a system for filtering and categorizing movie reviews. The goal is to train a model to automatically detect negative reviews. You'll be using a dataset of IMBD movie reviews with polarity labelling to build a model for classifying positive and negative reviews. It will need to reach an F1 score of at least 0.85.

## Description of the data

- `review`: the review text
- `pos: the target`, '0' for negative and '1' for positive
- `ds_part`: 'train'/'test' for the train/test part of dataset, correspondingly

## Answer these questions:

- Conduct an EDA and make your conclusion on the class imbalance.
- Preprocess the data for modeling.
- Train at least three different models for the given train dataset.
- Test the models for the given test dataset.
- Compose a few of your own reviews and classify them with all the models.
- Check for differences between the testing results of models in the above two points. Try to explain them.
- Present your findings.

## General conclusion

- The DummyClassifier, as expected, produces an F1 score of 50%, which is as good as flipping an unbiased coin.
- Comparing the LogisticRegression models with NLTK used for preprocessing and Spacy for preprocessing, the model with reviews preprocesed using NLTK, comes out at the top with best f1 score of 88%.
- Both the models were trained using 5 fold cross-validation with hyperparameter tuning on the C parameter.
- The LightGBM model turned out to have a lower f1 score, and it took more than two hours to complete training.
