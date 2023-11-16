## Project description

The data is stored in three files:

- gold_recovery_train.csv — training dataset download
- gold_recovery_test.csv — test dataset download
- gold_recovery_full.csv — source dataset download

Data is indexed with the date and time of acquisition (date feature). Parameters that are next to each other in terms of time are often similar.
Some parameters are not available because they were measured and/or calculated much later. That's why, some of the features that are present in the training set may be absent from the test set. The test set also doesn't contain targets.
The source dataset contains the training and test sets with all the features.
You have the raw data that was only downloaded from the warehouse. Before building the model, check the correctness of the data. For that, use our instructions.

## Description of the data

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

## Answer these questions:

- Check that recovery is calculated correctly. Using the training set, calculate recovery for the rougher.output.recovery feature. Find the MAE between your calculations and the feature values. Provide findings.
- Analyze the features not available in the test set. What are these parameters? What is their type?
- Perform data preprocessing.
- Take note of how the concentrations of metals (Au, Ag, Pb) change depending on the purification stage.
- Compare the feed particle size distributions in the training set and in the test set. If the distributions vary significantly, the model evaluation will be incorrect.
-  Consider the total concentrations of all substances at different stages: raw feed, rougher concentrate, and final concentrate. Do you notice any abnormal values in the total distribution? If you do, is it worth removing such values from both samples? Describe the findings and eliminate anomalies.
- Write a function to calculate the final sMAPE value.
- Train different models. Evaluate them using cross-validation. Pick the best model and test it using the test sample. Provide findings.

## General conclusion

We compared several models with Dummy Regressor (sMAPE=0.1029):
- Linear regression: 0.1238
- Decision tree regressor: nan
- Random forest regressor: 0.1177 with a 0.1047 score on the test set with 66% accuracy.
It seems that the Dummy Regressor has the best result according to the sMAPE
