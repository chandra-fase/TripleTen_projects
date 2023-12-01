## Project Description

This project focuses on analyzing data sourced from Instacart, a popular grocery delivery platform that allows customers to order groceries for home delivery, akin to the functionalities offered by Uber Eats or Door Dash.

The primary objective is to undertake data cleaning procedures, refining the dataset to ensure accuracy and reliability. Subsequently, the task is to compile a comprehensive report that delves into the shopping behaviors exhibited by Instacart customers.

## Key Project Tasks:

- Data Cleaning: Rigorous cleaning procedures to address inconsistencies, missing values, or any data irregularities within the Instacart dataset.

- Insight Generation: Utilizing cleaned data to extract valuable insights into the shopping habits of Instacart users. This includes identifying trends, preferences, or patterns within the dataset.

- Report Creation: Developing a comprehensive report summarizing your findings, supported by well-designed plots that effectively communicate your analysis results.

## Description of the Data

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

## General Conclusion

After analyzing the data, I concluded:
- Customers are doing the most shopping between 10am and around 3pm, and the customers shop more on Sunday and Monday.
- People are more likely to reorder their groceries monthly with most shoppers purchasing only one item and very little ordering over 15 items.

## Suggestions for the Company

Understanding customers' shopping habits regarding timing and frequency can significantly impact business strategies for Instacart or similar platforms. Here are some potential improvement ideas and business outcomes based on the conclusions drawn:

- **Optimized Delivery Scheduling:** Utilize the insights about peak shopping times (between 10 am to around 3 pm) to strategically plan delivery slots. Allocate more resources, delivery personnel, and customer support during these peak hours to ensure timely and efficient deliveries. This optimization could lead to increased customer satisfaction and loyalty.

- **Promotional Campaigns and Special Offers:** Leverage the findings regarding higher shopping frequencies on Sundays and Mondays. Design targeted promotional campaigns, discounts, or exclusive offers during these days to encourage more frequent shopping and increase order volumes during what seems to be naturally active shopping periods.

- **Reorder Incentives:** Given the observed tendency for customers to reorder monthly and purchase a relatively small number of items (with limited orders exceeding 15 items), introduce incentives or personalized recommendations for recurring monthly orders. Offering discounts or loyalty rewards for monthly reorders might encourage customers to stick to their routine purchases through Instacart.

- **User Experience Enhancements:** Simplify and streamline the ordering process for customers who tend to purchase few items. Focus on optimizing the interface, making it effortless for customers to place orders consisting of a limited number of items, potentially through quick-order options or personalized suggestions.

By implementing these strategies based on the observed shopping habits, Instacart or similar platforms can enhance user satisfaction, increase order frequency, and potentially drive higher revenue by catering to customers' preferences and shopping behaviors.
