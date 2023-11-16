## Project description

The focus of this project is to provide you with additional practice with common software engineering tasks. These will augment and complement your data skills, and make you a more attractive job candidate to potential employers.
The tasks are: creating and managing python virtual environments, developing a web application, and deploying it to a cloud service that will make it accessible to the public.
In this project, we are providing you with a dataset you are already familiar with: a dataset of car sales advertisements. 

## Description of the data

- `price` - price of the vehicle
- `model_year` - model year of the vehicle
- `model` - type of model
- `condition` - condition of the vehicle
- `cylinders` - number of cylinders
- `fuel` — gas, diesel, etc.
- `odometer` — the vehicle's mileage when the ad was published
- `transmission` - type of transmission
- `paint_color` - color of the vehicle
- `is_4wd` — whether the vehicle has 4-wheel drive (Boolean type)
- `date_posted` — the date the ad was published
- `days_listed` — from publication to removal

## Instructions for completing the project
Step 1. Project Prerequisites
1.	Create an account on github.com
2.	Create a new git repository with a README.md file and a .gitignore file (choose a Python template).
3.	Install at least the following packages: pandas, streamlit, plotly-express. Feel free to install more packages if you want to implement additional features in your web app.
4.	Create an account on render.com, link it to your GitHub account
5.	Install VS Code, load the project directory and set the Python interpreter to the one used by the virtual environment

Step 2. Download the data file
1.	Download the car advertisement dataset (vehicles_us.csv) or find your own dataset in a CSV format
2.	Place the dataset in the root directory of the project

Step 3. Exploratory Data Analysis
1.	Create an EDA.ipynb Jupyter notebook in VS Code
2.	Save the notebook in the notebooks directory of your project
3.	Perform some basic exploratory analysis of the dataset in the notebook
4.	Create a couple of histograms and scatterplots using plotly-express library

Step 4. Develop the web application dashboard
1.	Create an app.py file in the root of the project’s directory
2.	Import streamlit, pandas and plotly_express
3.	Read the dataset’s CSV file into a DataFrame

Step 5. Deploy the final version of the application to Render

## General conclusion

After taking care of the missing values within the dataset, we have a code to build a web app to narrow your search by filtering the data by age of the vehicle, and model type. This also allows you to see the way the price is reflected by different factors, including transmission, odometer, number of cylinders and the number of days listed.
