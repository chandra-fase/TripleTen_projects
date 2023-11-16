## Project description

The supermarket chain Good Seed would like to explore whether Data Science can help them adhere to alcohol laws by making sure they do not sell alcohol to people underage. You are asked to conduct that evaluation, so as you set to work, keep the following in mind:

- The shops are equipped with cameras in the checkout area which are triggered when a person is buying alcohol
- Computer vision methods can be used to determine age of a person from a photo
- The task then is to build and evaluate a model for verifying people's age

To start working on the task, you'll have a set of photographs of people with their ages indicated.

## Description of the data

- `file_name` - Name of the image
- `real_age` - Age of subject

## Answer these questions:

- Perform exploratory data analysis to get an overall impression of the dataset.
- Train and evaluate the model (it needs to be done on the GPU platform).
- Combine your code, output and findings (from the previous points) in the final Jupyter notebook.
- Make conclusions of the model evaluation, add them to the notebook.

## General conclusion

With our 20 epochs we were able to achieve a MAE of 5.5504, which is great. The system took less than 30 minutes to run, with each epoch taking just over one minute. This could possibly be further improved by adding dropout, and increasing the training time.
