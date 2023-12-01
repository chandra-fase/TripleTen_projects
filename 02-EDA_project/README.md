## Project description

This project focuses on analyzing data sourced from Instacart, a popular grocery delivery platform that allows customers to order groceries for home delivery, akin to the functionalities offered by Uber Eats or Door Dash.

The primary objective is to undertake data cleaning procedures, refining the dataset to ensure accuracy and reliability. Subsequently, the task is to compile a comprehensive report that delves into the shopping behaviors exhibited by Instacart customers.

## Key Project Tasks:

- Data Cleaning: Rigorous cleaning procedures to address inconsistencies, missing values, or any data irregularities within the Instacart dataset.

- Insight Generation: Utilizing cleaned data to extract valuable insights into the shopping habits of Instacart users. This includes identifying trends, preferences, or patterns within the dataset.

- Report Creation: Developing a comprehensive report summarizing your findings, supported by well-designed plots that effectively communicate your analysis results.

## Description of the data

There are five tables in the dataset, and you’ll need to use all of them to do your data preprocessing and EDA. Below is a data dictionary that lists the columns in each table and describes that data that hold.
- instacart_orders.csv: each row corresponds to one order on the Instacart app
  - `order_id`: ID number that uniquely identifies each order
  - `user_id`: ID number that uniquely identifies each customer account
  - `order_number`: the number of times this customer has placed an order
  - `order_dow`: day of the week that the order placed (which day is 0 is uncertain)
  - `order_hour_of_day`: hour of the day that the order was placed
  - `days_since_prior_order`: number of days since this customer placed their previous order
- products.csv: each row corresponds to a unique product that customers can buy
  - `product_id`: ID number that uniquely identifies each product
  - `product_name`: name of the product
  - `aisle_id`: ID number that uniquely identifies each grocery aisle category
  - `department_id`: ID number that uniquely identifies each grocery department category
- order_products.csv: each row corresponds to one item placed in an order
  - `order_id`: ID number that uniquely identifies each order
  - `product_id`: ID number that uniquely identifies each product
  - `add_to_cart_order`: the sequential order in which each item was placed in the cart
  - `reordered`: 0 if the customer has never ordered this product before, 1 if they have
- aisles.csv
  - `aisle_id`: ID number that uniquely identifies each grocery aisle category
  - `aisle`: name of the aisle
- departments.csv
  - `department_id`: ID number that uniquely identifies each grocery department category
  - `department`: name of the department

## General conclusion

After analyzing the data, I concluded:
- Customers are doing the most shopping between 10am and around 3pm, and the customers shop more on Sunday and Monday.
- People are more likely to reorder their groceries monthly with most shoppers purchasing only one item and very little ordering over 15 items.
