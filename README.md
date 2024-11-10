
# Customer Orders Dataset Analysis

This repository provides a sample dataset of customer orders and includes queries for analyzing customer purchasing behaviors. Each query addresses a specific scenario, showcasing data filtering, grouping, joining, deduplication, sorting, and aggregation.

## Dataset Structure

The dataset consists of customer order records with the following columns:

| Column      | Data Type   | Description                           |
|-------------|-------------|---------------------------------------|
| customer_id | int         | Unique ID for each customer          |
| name        | chararray   | Name of the customer                 |
| age         | int         | Age of the customer                  |
| location    | chararray   | Location of the customer             |
| order_id    | int         | Unique order ID                      |
| order_date  | chararray   | Date the order was placed (YYYY-MM-DD)|
| amount      | float       | Order amount in dollars              |

### Sample Data

| customer_id | name    | age | location   | order_id | order_date | amount |
|-------------|---------|-----|------------|----------|------------|--------|
| 101         | Alice   | 25  | New York   | 1001     | 2023-01-05 | 150.00 |
| 102         | Bob     | 30  | San Diego  | 1002     | 2023-02-10 | 220.50 |
| ...         | ...     | ... | ...        | ...      | ...        | ...    |

## Analysis Scenarios and Queries

### 1. Filtering Customers by Age
**Scenario:** Analyze customers who are adults (age 18 and above).
- **Query:** Load the dataset and filter out customers with `age < 18`.

![1](https://github.com/user-attachments/assets/da2588ef-7b73-4388-8b11-1e6e44a44243)


### 2. Grouping by Customer and Calculating Total Sales
**Scenario:** Calculate the total order amount for each customer.
- **Query:** Group the data by `customer_id` and calculate the total sales (sum of `amount`) for each customer.

  ![2](https://github.com/user-attachments/assets/442d66d1-3dd0-4bad-9d3a-e374f3665fb3)


### 3. Joining Orders with Customer Information
**Scenario:** Combine customer details with order information for a detailed view.
- **Query:** Join the dataset with itself on `customer_id` to display `order_id`, `name`, `location`, and `order_date`.
  
![3](https://github.com/user-attachments/assets/edf0a6aa-d88a-45c4-8294-d106766d193a)

### 4. Removing Duplicate Orders
**Scenario:** Remove duplicate records due to potential system errors.
- **Query:** Load the dataset and remove any duplicate entries based on `order_id`.
  
![4](https://github.com/user-attachments/assets/dd0a95bf-19eb-427b-b859-6c905aadddcd)

### 5. Sorting Orders by Amount
**Scenario:** Identify the highest value orders.
- **Query:** Load the dataset, sort by `amount` in descending order, and display the top 3 highest orders.
  
![5](https://github.com/user-attachments/assets/8a0932f7-e05e-4665-8bc6-4b390700d05c)

### 6. Aggregating and Filtering Data (Total Purchases Above $500)
**Scenario:** Identify customers whose total purchases exceed $500.
- **Query:** Group orders by `customer_id`, calculate the total purchase amount, and filter for customers who spent more than $500.

  ![6](https://github.com/user-attachments/assets/6cc697a2-fc4f-4e47-a930-c8dca38cd03e)


