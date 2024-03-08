# Superstore_Analysis
In this repository, I present an analysis of the "superstore_sales.xlsx" file. This dataset contains comprehensive information about orders made in a superstore. The analysis is conducted using Python, leveraging popular libraries such as Pandas, Seaborn, and Matplotlib.
# Notebook Overview
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
```
The analysis includes:

- Grouping data using groupby to derive insights.
- Creating bar plots and scatter plots to visualize trends and patterns in the data.
- Implementing RFM (Recency, Frequency, Monetary) analysis for customer segmentation.
# Dataset Description
| Column Name     | Description                                     |
|-----------------|-------------------------------------------------|
| order_id        | Unique identifier for each order.               |
| order_date      | Date when the order was placed.                 |
| ship_date       | Date when the order was shipped.                |
| ship_mode       | Mode of shipping for the order.                 |
| customer_name   | Name of the customer placing the order.         |
| segment         | Market segment to which the customer belongs.   |
| state           | State where the order was placed.               |
| country         | Country where the order was placed.             |
| market          | Market where the order was made.                |
| region          | Region where the order was placed.              |
| product_id      | Unique identifier for each product.             |
| category        | Category of the product.                        |
| sub_category    | Sub-category of the product.                    |
| product_name    | Name of the product.                            |
| sales           | Sales amount for the order.                     |
| quantity        | Quantity of products ordered.                   |
| discount        | Discount applied to the order.                  |
| profit          | Profit generated from the order.                |
| shipping_cost   | Shipping cost for the order.                    |
| order_priority  | Priority of the order.                          |
| year            | Year in which the order was placed.             |


This analysis aims to uncover insights into sales patterns, customer behavior, and overall performance of the superstore.
