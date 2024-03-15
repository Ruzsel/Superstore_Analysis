# Superstore_Analysis
In this repository, I present an analysis of the "superstore_sales.xlsx" file. This dataset contains comprehensive information about orders made in a superstore. The analysis is conducted using Python, leveraging popular libraries such as Pandas, Seaborn, and Matplotlib.
## Notebook Overview
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
```
The analysis includes:

- Grouping data using groupby to derive insights.
- Creating bar plots and scatter plots to visualize trends and patterns in the data.
- Implementing RFM (Recency, Frequency, Monetary) analysis for customer segmentation.
## Dataset Description
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

## Data Analysis

### Importing Libraries
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
from datetime import date
```
Read csv file
```python
df = pd.read_excel('superstore_sales.xlsx')
```
```python
df.shape
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/3defb160-079f-4db7-8587-26a68e005f3b)
```python
df.sample(5)
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/5ff8c517-8882-493f-b277-ebc94424d27d)

checking null value
```python
df.isnull().sum()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/10d17982-d488-4669-87cd-df164fcf6000)

Knowing the data
```python
df.info()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/b84cc34f-9dfd-4795-a373-05ac08298a50)

group by 'product_name'
```python
df.groupby(['product_name']).agg({'sales': 'sum', 'quantity': 'sum', 'profit': 'sum', 'shipping_cost': 'sum'})
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/d5cf0997-ae1c-4083-b0c7-96cd8a3850ad)

Create a variable that displays sales grouped by subcategory, then only display the top 5 from that variable
```python
Subcategory_product_sales = df.groupby('sub_category')['sales'].sum().reset_index()
Subcategory_product_sales = Subcategory_product_sales.nlargest(5, 'sales')
Subcategory_product_sales
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/4755ae28-63f3-466d-a313-3429930d57c4)

Create a horizontal bar plot illustrating the top 5 subcategories based on their total sales. It first sets the figure size, then generates the bar plot with subcategory names on the y-axis and corresponding sales values on the x-axis
```python
plt.figure(figsize=(10, 6))
plt.barh(Subcategory_product_sales['sub_category'], Subcategory_product_sales['sales'], color='skyblue')
plt.xlabel('Total Sales')
plt.ylabel('Sub Category')
plt.title('Top 5 Sub Category by Total Sales')
plt.gca().invert_yaxis()
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/ec95ef5b-4919-478b-babc-303c986a01d5)

Calculate total sales for each 'product_name'. Select the top 5 products based on their sales and display the top 5 products with their sales data.
```python
product_name_sales = df.groupby('product_name')['sales'].sum().reset_index()
product_name_sales = product_name_sales.nlargest(5, 'sales')
product_name_sales
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/69d24b3f-2f79-4264-96c9-41c975945f99)

Generate a horizontal bar plot illustrating the top 5 products based on their total sales. It first sets the figure size, then creates the bar plot with product names on the y-axis and corresponding sales values on the x-axis.
```python
plt.figure(figsize=(10, 6))
plt.barh(product_name_sales['product_name'], product_name_sales['sales'], color='skyblue')
plt.xlabel('Total Sales')
plt.ylabel('Product Name')
plt.title('Top 5 Products by Total Sales')
plt.gca().invert_yaxis()
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/3a1ada70-0313-42b7-a572-b383fbb4e09b)

Calculates the total profit for each subcategory, then selects the top 5 subcategories with the highest profits. Finally, it displays the resulting DataFrame containing the top 5 subcategories by profit.
```python
Subcategory_profit = df.groupby('sub_category')['profit'].sum().reset_index()
Subcategory_profit = Subcategory_profit.nlargest(5, 'profit')
Subcategory_profit
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/a1087612-ca06-4aa4-8a99-d5b36025f1e6)

Create a horizontal bar plot, depicting the top 5 subcategories based on their total profit. It sets the figure size to 10x6 inches, creates the bar plot with subcategory names on the y-axis and corresponding profit values on the x-axis.
```python
plt.figure(figsize=(10, 6))
plt.barh(Subcategory_profit['sub_category'], Subcategory_profit['profit'], color='darkgreen')
plt.xlabel('Total Profit')
plt.ylabel('Sub Category')
plt.title('Top 5 Sub Category by Total Profit')
plt.gca().invert_yaxis()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/3211bf1e-3e66-470c-8bcb-82a5b581bc69)

Calculates the total profit for each product name, then selects the top 5 products with the highest profits. Finally, it displays the resulting DataFrame containing the top 5 products by profit.
```python
product_name_profit = df.groupby('product_name')['profit'].sum().reset_index()
product_name_profit = product_name_profit.nlargest(5, 'profit')
product_name_profit
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/c89323e8-6502-4841-badb-7b51aa004be9)

Generate a horizontal bar plot representing the top 5 products based on their total profit. It sets the figure size to 10x6 inches, creates the bar plot with product names on the y-axis and corresponding profit values on the x-axis. The bars are colored dark green, and the axes are labeled accordingly. 
```python
plt.figure(figsize=(10, 6))
plt.barh(product_name_profit['product_name'], product_name_profit['profit'], color='darkgreen')
plt.xlabel('Total Profit')
plt.ylabel('Product Name')
plt.title('Top 5 Products by Total Profit')
plt.gca().invert_yaxis()
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/0739a8dd-0fcb-42a5-9ec6-347b3e345dcc)

Generates a DataFrame by grouping the original DataFrame 'df' by the 'category' and 'sub_category' columns and then summing up the quantities for each group. Only numeric columns are considered for the summation.
```python
pd.DataFrame(df.groupby(['category', 'sub_category']).sum(numeric_only=True)['quantity'])
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/9d1c7d4e-a805-4cd3-9f95-e30ad26eb74b)

Utilizes Seaborn to create a FacetGrid plot, where each column represents a different 'ship_mode'. For each column, a histogram is plotted depicting the distribution of categories ('category'). The 'top' parameter in 'plt.subplots_adjust' adjusts the space at the top of the plot to accommodate the main title, which is set to 'Distribution of Categories by Ship Mode'. 
```python
category_name = sns.FacetGrid(df, col='ship_mode')
category_name.map(plt.hist, 'category')
plt.subplots_adjust(top=0.85)
category_name.fig.suptitle('Distribution of Categories by Ship Mode')
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/c14e1d21-dce8-483c-b7b7-aac1c65a8a55)

Generates a bar plot showing the count of users for each 'ship_mode'. It sets the figure size to 10x6 inches and creates bars with heights corresponding to the number of users for each ship mode. Grid lines are added along the y-axis with dashed lines for reference. Additionally, text annotations displaying the exact counts are placed at the top of each bar
```python
ship_mode_counts = df['ship_mode'].value_counts()

plt.figure(figsize=(10, 6))
bars = plt.bar(ship_mode_counts.index, ship_mode_counts.values, color='skyblue')

plt.xlabel('Ship Mode')
plt.ylabel('Total User')
plt.title('Most Used Ship Mode')
plt.xticks(rotation=45, ha='right')
plt.grid(axis='y', linestyle='--', alpha=0.7)

for bar in bars:
    yval = bar.get_height()
    plt.text(bar.get_x() + bar.get_width()/2, yval, int(yval), va='bottom', ha='center')

plt.tight_layout()
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/87a8d679-54f2-4366-9738-7bda999436b4)

Calculates the total sales for each segment, selects the top 3 segments with the highest sales, and then displays the resulting DataFrame containing the top 3 segments by sales.
```python
segment_sales = df.groupby('segment')['sales'].sum().reset_index()
segment_sales = segment_sales.nlargest(3, columns= 'sales')
segment_sales
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/8f0d7c6b-f091-4b45-9f3a-aaceda87e98e)

Creates a horizontal bar plot using Seaborn (sns.barplot) to visualize the total sales for the top 3 segments. The x parameter specifies the sales values, while the y parameter specifies the segment categories. The hue parameter is set to 'sales' to color the bars based on the sales values. 
```python
plt.figure(figsize=(10, 6))
sns.barplot(x='sales', y='segment', data=segment_sales, hue='sales', palette='viridis', legend=False)
plt.xlabel('Total Sales')
plt.ylabel('Segment')
plt.title('Top 3 Segments by Total Sales')
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/3fa72feb-4d8c-4793-950a-f581e72bd018)

Code calculates the total profit for each segment, selects the top 3 segments with the highest profit, and then displays the resulting DataFrame containing the top 3 segments by profit.
```python
segment_profit = df.groupby('segment')['profit'].sum().reset_index()
segment_profit = segment_profit.nlargest(3, columns= 'profit')
segment_profit
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/5c4f55dd-8ec2-4bfb-8e77-23db5abc4979)

Creates a horizontal bar plot using Seaborn (sns.barplot) to visualize the total profit for the top 3 segments. The x parameter specifies the profit values, while the y parameter specifies the segment categories. The hue parameter is set to 'profit' to color the bars based on the profit values. The color palette 'viridis' is used for coloring the bars. The legend is turned off (legend=False).
```python
plt.figure(figsize=(10, 6))
sns.barplot(x='profit', y='segment', data=segment_profit, hue='profit', palette='viridis', legend=False)
plt.xlabel('Total Profit')
plt.ylabel('Segment')
plt.title('Top 3 Segments by Total Profit')
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/170c1c72-b3e7-46f9-8334-23f7c570f0b4)

Calculates the total profit for each year by grouping the DataFrame 'df' based on the 'year' column and summing up the profits.
```python
profit_by_year = df.groupby('year')['profit'].sum()
```
Code generates a bar plot to visualize the total profit by year. It sets the figure size to 10x6 inches and creates bars with heights corresponding to the total profit for each year. The bars are colored dark green. Text annotations displaying the exact profit values are placed at the top of each bar.
```python
plt.figure(figsize=(10, 6))
bars = plt.bar(profit_by_year.index, profit_by_year.values, color='darkgreen')

for bar in bars:
    yval = bar.get_height()
    plt.text(bar.get_x() + bar.get_width()/2, yval, int(yval), va='bottom', ha='center')

plt.xlabel('Year')
plt.ylabel('Total Profit')
plt.title('Total Profit By Year')
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/b3308540-1f13-4a39-8619-3ab3cf4cd14b)

Calculates the total sales for each year by grouping the DataFrame 'df' based on the 'year' column and summing up the sales.
```python
sales_by_year = df.groupby(df['year'])['sales'].sum()
```
Generates a bar plot to visualize the total sales by year. It sets the figure size to 10x6 inches and creates bars with heights corresponding to the total sales for each year. The bars are colored sky blue. Text annotations displaying the exact sales values are placed at the top of each bar. The x-axis represents the years, and the y-axis represents the total sales.
```python
plt.figure(figsize=(10, 6))
bars = plt.bar(sales_by_year.index, sales_by_year.values, color='skyblue')

for bar in bars:
    yval = bar.get_height()
    plt.text(bar.get_x() + bar.get_width()/2, yval, int(yval), va='bottom', ha='center')

plt.xlabel('Year')
plt.ylabel('Total Sales')
plt.title('Sales by Year')
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/9059fce2-3aaf-4fa9-a144-d481bf7bed0e)

Calculates the total profit for each country, then selects the top 10 countries with the highest profit, and finally displays the resulting DataFrame containing the top 10 countries by profit.
```python
profit_by_country = df.groupby('country')['profit'].sum().reset_index()
top_profit_by_country = profit_by_country.nlargest(10, 'profit')
top_profit_by_country
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/972a0de2-c035-4888-9684-44dd93b0ad91)

Generates a bar plot to visualize the total profit for the top 10 countries. It sets the figure size to 12x6 inches and creates bars with heights corresponding to the total profit for each country. The bars are colored dark green. The x-axis represents the countries, and the y-axis represents the total profit. The plot is titled 'Total 10 Profit by Country'. X-axis labels are rotated by 45 degrees and aligned to the right for better readability.
```python
plt.figure(figsize=(12, 6))
bars = plt.bar(top_profit_by_country['country'], top_profit_by_country['profit'], color='darkgreen')
plt.xlabel('Country')
plt.ylabel('Total Profit')
plt.title('Total 10 Profit by Country')
plt.xticks(rotation=45, ha='right')
plt.grid(axis='y', linestyle='--', alpha=0.7)

for bar in bars:
    yval = bar.get_height()
    plt.text(bar.get_x() + bar.get_width()/2, yval, round(yval, 2), va='bottom', ha='center')

plt.tight_layout()
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/f4d21e3c-4c41-425a-a895-895239e2254b)

Calculates the total sales for each country, then selects the top 10 countries with the highest sales, and finally displays the resulting DataFrame containing the top 10 countries by sales.
```python
sales_by_country = df.groupby('country')['sales'].sum().reset_index()
top_sales_by_country = sales_by_country.nlargest(10, 'sales')
```
Generates a bar plot to visualize the total sales for the top 10 countries. It sets the figure size to 12x6 inches and creates bars with heights corresponding to the total sales for each country. The bars are colored sky blue. The x-axis represents the countries, and the y-axis represents the total sales. The plot is titled 'Top 10 Sales by Country'. X-axis labels are rotated by 45 degrees and aligned to the right for better readability. 
```python
plt.figure(figsize=(12, 6))
bars = plt.bar(top_sales_by_country['country'], top_sales_by_country['sales'], color='skyblue')
plt.xlabel('Country')
plt.ylabel('Total Sales')
plt.title('Top 10 Sales by Country')
plt.xticks(rotation=45, ha='right')
plt.grid(axis='y', linestyle='--', alpha=0.7)

for bar in bars:
    yval = bar.get_height()
    plt.text(bar.get_x() + bar.get_width()/2, yval, round(yval, 2), va='bottom', ha='center')

plt.tight_layout()
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/4410c74c-9584-4406-887c-a3acbeb98881)

## RFM Analysis
Provide code performs RFM (Recency, Frequency, Monetary) analysis on customer data:

1. **Recency Calculation**: It calculates the recency for each customer by finding the maximum order date for each customer and then subtracting it from the overall maximum order date to get the number of days since their last purchase.

2. **Frequency Calculation**: It calculates the frequency for each customer by counting the unique order IDs associated with each customer.

3. **Monetary Calculation**: It calculates the monetary value for each customer by summing up the sales amount for each customer.

4. **Merging DataFrames**: It merges the recency, frequency, and monetary DataFrames based on the 'customer_name' column to create the RFM DataFrame.

5. **Printing the RFM DataFrame**: It displays the first few rows of the RFM DataFrame.

This process helps in segmenting customers based on their recent purchase behavior, purchase frequency, and monetary value.
```python
#RFM Analysis
recency = df.groupby('customer_name')['order_date'].max().reset_index()
recency['recency'] = (df['order_date'].max() - recency['order_date']).dt.days

frequency = df.groupby('customer_name')['order_id'].nunique().reset_index()
frequency.columns = ['customer_name', 'frequency']

monetary = df.groupby('customer_name')['sales'].sum().reset_index()
monetary.columns = ['customer_name', 'monetary']

rfm = pd.merge(recency, frequency, on='customer_name')
rfm = pd.merge(rfm, monetary, on='customer_name')

print(rfm.head())
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/d18fc9d3-d8f7-4932-9296-edea3662cc38)

Provide code plots three scatter plots based on RFM analysis:

1. **Recency vs Frequency**:
   - X-axis: Recency (days since last purchase)
   - Y-axis: Frequency (number of orders)
   - Each point represents a customer.
   - Blue color is used for the points.

2. **Monetary vs Frequency**:
   - X-axis: Monetary (total sales amount)
   - Y-axis: Frequency (number of orders)
   - Each point represents a customer.
   - Green color is used for the points.

3. **Recency vs Monetary**:
   - X-axis: Recency (days since last purchase)
   - Y-axis: Monetary (total sales amount)
   - Each point represents a customer.
   - Red color is used for the points.

All plots have grid lines for better visualization. These plots help in understanding the relationships between recency, frequency, and monetary value, which are crucial for customer segmentation and targeted marketing strategies.
```python
# Plot Recency vs Frequency
plt.figure(figsize=(12, 6))
plt.scatter(rfm['recency'], rfm['frequency'], color='blue', alpha=0.5)
plt.xlabel('Recency (days)')
plt.ylabel('Frequency (orders)')
plt.title('Recency vs Frequency')
plt.grid(True)
plt.show()

# Plot Monetary vs Frequency
plt.figure(figsize=(12, 6))
plt.scatter(rfm['monetary'], rfm['frequency'], color='green', alpha=0.5)
plt.xlabel('Monetary (sales)')
plt.ylabel('Frequency (orders)')
plt.title('Monetary vs Frequency')
plt.grid(True)
plt.show()

# Plot Recency vs Monetary
plt.figure(figsize=(12, 6))
plt.scatter(rfm['recency'], rfm['monetary'], color='red', alpha=0.5)
plt.xlabel('Recency (days)')
plt.ylabel('Monetary (sales)')
plt.title('Recency vs Monetary')
plt.grid(True)
plt.show()
```
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/33935ad7-7e01-4708-a019-d27b62961b88)
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/c04a6f03-6fc6-490e-bb4c-ff200d71dafe)
![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/865ebb61-a1a7-4e4b-a1f1-3a276fbecc7d)
