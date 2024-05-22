# Project Overview
this project revolves around exploring and analyzing a dataset to derive meaningful insights and inform decision-making. The primary focus is on understanding the data, performing various analyses, and visualizing the findings to communicate key observations effectively.

# About this Project
The project centers on a comprehensive analysis of a dataset encompassing various aspects such as sales, customer information, product details, and market segments. Key tasks undertaken include data validation, exploratory data analysis (EDA), statistical analysis, and visualization of trends and patterns within the dataset.

# Objective
The main objective of this project is to extract actionable insights from the dataset to drive business decisions and strategies. Through rigorous analysis and visualization, the aim is to uncover trends, identify opportunities, and address challenges within the data.

# User Story
As a data analyst, I meticulously validated the dataset to ensure data quality and integrity. This involved checking for missing values, duplicates, descriptive statistics, and ensuring proper data formats. By leveraging advanced analytical techniques, I aimed to uncover hidden patterns and correlations that could guide strategic decision-making.

# Additional Sections
- Data Validation: Detail the steps taken to validate the dataset, including checking for missing values, duplicates, descriptive statistics and ensuring proper data formats. [Click Here](#import-library)
- Exploratory Data Analysis (EDA): Provide insights from the initial exploration of the dataset, including summary statistics, distributions, and correlations between variables.
- Statistical Analysis: Discuss any statistical tests or analyses conducted to validate findings or test hypotheses within the dataset.
- Visualization: Showcase visualizations created to represent key insights and trends discovered during the analysis process.
- Key Findings: Summarize the most significant findings and insights derived from the analysis, highlighting actionable recommendations or areas for further investigation.
- Insight and Business Solution : Reflect on the overall analysis process, lessons learned, and the impact of insights on potential business outcomes. [Click Here](#findings-and-business-solution)

# EDA (Exploratory Data Analysis)
1. Annual Sales and Profit Trend : Observing the sales and profit trend from year to year. [Click Here](#1-annual-sales-and-profit-trend)
2. Sales by Product Category : Identifying the most popular product category. and breakdown top 5 `product_name` from that category. [Click Here](#2-sales-by-product-category)
3. Distribution of Shipping Modes : Observing how shipping modes are distributed. [Click Here](#3-distribution-of-shipping-modes)
4. Income by Country/Region : Identifying which country or region provides the highest income. [Click Here](#4-income-by-countryregion)
5. Customer Purchase Frequency : Understanding how often customers make purchases. [Click Here](#5-customer-purchase-frequency)
6. Order Priority Distribution : Observing how order priorities are distributed. [Click Here](#6-order-priority-distribution)
7. Correlation between Discount and Profit : Determining if there's a correlation between the amount of discount given and the profit earned. [Click Here](#7-correlation-between-discount-and-profit)
8. Monthly Profit(Discount Apply) : Viewing profit per month for each year. [Click Here](#8-monthly-profitdiscount-apply)
9. Average Profit(Discount Apply) per Order : Calculating the average profit obtained from each order without outliers. [Click Here](#9-average-profitdiscount-apply-per-order)
10. RFM Analysis : Determining customer segmentation based on Recency, Frequency, and Monetary. [Click Here](#10-rfm-analysis)
11. Sales Distribution by Customer Segment : This section provides an overview of the distribution of sales revenue across different customer segments.[Click Here](#11-sales-distribution-by-customer-segment)

# About the Data

## Superstore Sales Data: Column Descriptions

| Column Name     | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| order_id        | Unique identifier for each order                                            |
| order_date      | The date when the order was placed                                          |
| ship_date       | The date when the order was shipped                                         |
| ship_mode       | The mode of shipment (e.g., Standard Class, Second Class, Same Day)         |
| customer_name   | The name of the customer who placed the order                               |
| segment         | The segment of the customer (e.g., Consumer, Corporate, Home Office)        |
| state           | The state or province where the customer is located                         |
| country         | The country where the customer is located                                   |
| market          | The market region (e.g., APAC, EMEA, EU)                                    |
| region          | The specific region within the market (e.g., North, South, Oceania)         |
| product_id      | Unique identifier for each product                                          |
| category        | The category of the product (e.g., Office Supplies, Furniture, Technology)  |
| sub_category    | The sub-category of the product (e.g., Storage, Paper, Appliances)          |
| product_name    | The name of the product                                                     |
| sales           | The sales amount for the order                                              |
| quantity        | The quantity of the product ordered                                         |
| discount        | The discount applied to the order                                           |
| profit          | The profit earned from the order                                            |
| shipping_cost   | The cost of shipping the order                                              |
| order_priority  | The priority level of the order (e.g., High, Medium, Low, Critical)         |
| year            | The year when the order was placed                                          |


## 10 Sample for each columns

| order_id      | order_date | ship_date | ship_mode     | customer_name   | segment       | state          | country   | market | region     | product_id       | category       | sub_category | product_name                                | sales | quantity | discount | profit  | shipping_cost | order_priority | year |
|---------------|------------|-----------|---------------|-----------------|---------------|----------------|-----------|--------|------------|------------------|----------------|--------------|---------------------------------------------|-------|----------|----------|---------|---------------|----------------|------|
| AG-2011-2040  | 1/1/2011   | 1/6/2011  | Standard Class| Toby Braunhardt| Consumer      | Constantine    | Algeria   | Africa | Africa     | OFF-TEN-10000025 | Office Supplies| Storage      | Tenex Lockers, Blue                        | 408   | 2        | 0        | 106.14  | 35.46         | Medium         | 2011 |
| IN-2011-47883 | 1/1/2011   | 1/8/2011  | Standard Class| Joseph Holt     | Consumer      | New South Wales| Australia | APAC   | Oceania    | OFF-SU-10000618  | Office Supplies| Supplies     | Acme Trimmer, High Speed                   | 120   | 3        | 0.1      | 36.036  | 9.72          | Medium         | 2011 |
| HU-2011-1220  | 1/1/2011   | 1/5/2011  | Second Class  | Annie Thurman   | Consumer      | Budapest       | Hungary   | EMEA   | EMEA       | OFF-TEN-10001585 | Office Supplies| Storage      | Tenex Box, Single Width                    | 66    | 4        | 0        | 29.64   | 8.17          | High           | 2011 |
| IT-2011-3647632| 1/1/2011   | 1/5/2011  | Second Class  | Eugene Moren    | Home Office   | Stockholm      | Sweden    | EU     | North      | OFF-PA-10001492  | Office Supplies| Paper        | Enermax Note Cards, Premium                | 45    | 3        | 0.5      | -26.055 | 4.82          | High           | 2011 |
| IN-2011-47883 | 1/1/2011   | 1/8/2011  | Standard Class| Joseph Holt     | Consumer      | New South Wales| Australia | APAC   | Oceania    | FUR-FU-10003447  | Furniture      | Furnishings | Eldon Light Bulb, Duo Pack                 | 114   | 5        | 0.1      | 37.77   | 4.70          | Medium         | 2011 |
| IN-2011-47883 | 1/1/2011   | 1/8/2011  | Standard Class| Joseph Holt     | Consumer      | New South Wales| Australia | APAC   | Oceania    | OFF-PA-10001968  | Office Supplies| Paper        | Eaton Computer Printout Paper, 8.5 x 11  | 55    | 2        | 0.1      | 15.342  | 1.80          | Medium         | 2011 |
| CA-2011-1510  | 1/2/2011   | 1/6/2011  | Standard Class| Magdelene Morse | Consumer      | Ontario        | Canada    | Canada | Canada     | TEC-OKI-10002750 | Technology     | Machines     | Okidata Inkjet, Wireless                   | 314   | 1        | 0        | 3.12    | 24.10         | Medium         | 2011 |
| IN-2011-79397 | 1/3/2011   | 1/3/2011  | Same Day      | Kean Nguyen    | Corporate     | New South Wales| Australia | APAC   | Oceania    | OFF-AP-10000304  | Office Supplies| Appliances   | Hoover Microwave, White                    | 276   | 1        | 0.1      | 110.412 | 125.32        | Critical       | 2011 |
| ID-2011-80230  | 1/3/2011   | 1/9/2011  | Standard Class| Ken Lonsdale    | Consumer      | Auckland       | New Zealand| APAC   | Oceania    | TEC-CO-10004182  | Technology     | Copiers      | Hewlett Wireless Fax, Laser                | 912   | 4        | 0.4      | -319.464| 107.1         | Low            | 2011 |

# Import Library
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np
import datetime as dt
from datetime import date
from scipy.stats import mode
```

```python
df = pd.read_excel('superstore_sales.xlsx')
```

# Data Quality Check
## Missing Values
```python
print(df.isnull().sum())
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/bb85f82c-569e-47e1-bec6-7e3159fbbef7)

---

## Data type
```python
df.dtypes
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/87dd5ab8-d957-4a97-b7d5-705424223a08)

---

## Descriptive Statistics
```python
print(df.describe())
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/f406bf32-79f7-4f51-9624-33d23a5a90ae)

---

## Duplicate Check
```python
duplicate_rows = df.duplicated()

print("Duplicate Rows(True):", duplicate_rows.sum())
print("Duplicate Rows(False):", (len(duplicate_rows) - duplicate_rows.sum()))
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/4fcba36b-7a8b-46ca-aa22-e8c69ec6628c)

---

## 1. Annual Sales and Profit Trend

```python
yearly_sales = df.groupby('year')['sales'].sum()
ax = yearly_sales.plot(kind='bar',color='darkblue', xlabel='Year', ylabel='Total Sales', title='Year to Year Sales Trend')

for i, v in enumerate(yearly_sales):
    ax.text(i, v + 0.03 * v, '${:,.0f}'.format(v), ha='center', va='bottom')
ax.set_ylim(0, max(yearly_sales) * 1.1)
ax.set_xticklabels(yearly_sales.index, rotation=45, ha='right')
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/e9fd5412-05e8-444a-899c-f6275eb8940b)


```python
yearly_profit = df.groupby('year')['profit'].sum()
ax = yearly_profit.plot(kind='bar',color='green', xlabel='Year', ylabel='Total profit', title='Year to Year profit Trend')

for i, v in enumerate(yearly_profit):
    ax.text(i, v + 0.03 * v, '${:,.0f}'.format(v), ha='center', va='bottom')
ax.set_ylim(0, max(yearly_profit) * 1.1)
ax.set_xticklabels(yearly_profit.index, rotation=45, ha='right')
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/e120c3d5-8b31-4a47-ac97-16d2f324ce75)

---

## 2. Sales by Product Category

```python
category_sales = df.groupby('category')['sales'].sum().sort_values(ascending=False)
ax = category_sales.plot(kind='bar',color='darkblue', xlabel='Product Category', ylabel='Total Sales', title='Sales by Product Category')

for i, v in enumerate(category_sales):
    ax.text(i, v + 0.03 * v, '${:,.0f}'.format(v), ha='center', va='bottom')

ax.set_ylim(0, max(category_sales) * 1.1)
ax.set_xticklabels(category_sales.index, rotation=45, ha='right')
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/069a38e0-13fe-41bb-86a6-386565b3b853)

```python
#def function for shorter 'product_name' value names
def shorten_name(name, max_length=30):
    if len(name) > max_length:
        return name[:max_length] + '...'
    else:
        return name

# data filter for each category
technology_data = df[df['category'] == 'Technology']
furniture_data = df[df['category'] == 'Furniture']
office_supplies_data = df[df['category'] == 'Office Supplies']

# Function to get top 5 product_name
def get_top_products(data):
    top_products = data.groupby('product_name')['sales'].sum().sort_values(ascending=False).head(5)
    top_products.index = top_products.index.map(shorten_name)
    return top_products

# Top 5 Product for each category
top_tech_products = get_top_products(technology_data)
top_furniture_products = get_top_products(furniture_data)
top_office_supplies_products = get_top_products(office_supplies_data)
```

```python
# Plot bar chart for each category
fig, axs = plt.subplots(3, 1, figsize=(12, 18))

# Technology
axs[0].barh(top_tech_products.index, top_tech_products.values, color='skyblue')
axs[0].set_title('Top 5 Product - Technology')
axs[0].set_xlabel('Total Sales (K)')
axs[0].set_ylabel('Product Name')
for i, v in enumerate(top_tech_products.values):
    axs[0].text(v + 0.01 * v, i, '${:,.0f}K'.format(v / 1000), color='blue', va='center')

# Furniture
axs[1].barh(top_furniture_products.index, top_furniture_products.values, color='lightgreen')
axs[1].set_title('Top 5 Product - Furniture')
axs[1].set_xlabel('Total Sales (K)')
axs[1].set_ylabel('Product Name')
for i, v in enumerate(top_furniture_products.values):
    axs[1].text(v + 0.01 * v, i, '${:,.0f}K'.format(v / 1000), color='green', va='center')

# Office Supplies
axs[2].barh(top_office_supplies_products.index, top_office_supplies_products.values, color='salmon')
axs[2].set_title('Top 5 Product - Office Supplies')
axs[2].set_xlabel('Total Sales (K)')
axs[2].set_ylabel('Product Name')
for i, v in enumerate(top_office_supplies_products.values):
    axs[2].text(v + 0.01 * v, i, '${:,.0f}K'.format(v / 1000), color='red', va='center')

# add padding on left corner
plt.subplots_adjust(left=0.3, right=0.9, top=0.9, bottom=0.1)

plt.tight_layout()
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/49056a7c-3002-4690-b679-a37ec7d5d749)

---

## 3. Distribution of Shipping Modes

```python
sns.countplot(x='ship_mode', data=df, color='skyblue')
plt.title('Shipping Mode Distribution')

for p in plt.gca().patches:
    plt.gca().annotate('{:,.0f}'.format(p.get_height()), (p.get_x() + p.get_width() / 2., p.get_height()), 
                       ha='center', va='bottom', xytext=(0, 5), textcoords='offset points')

plt.ylim(0, max(df['ship_mode'].value_counts()) * 1.1)
plt.xlabel('Ship Mode')
plt.ylabel('Total Shipment')
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/0f2c2968-8173-4819-8777-ffa3790f34e7)

---

## 4. Income by Country/Region

```python
def format_thousands(x):
    return '${:.1f}K'.format(x / 1000)

top_10_countries_profit = df.groupby('country')['profit'].sum().sort_values(ascending=False).head(10)

ax = top_10_countries_profit.plot(kind='barh',color='green', xlabel='Total profit', ylabel='Country', title='Profit by Country (Top 10)')

for i, v in enumerate(top_10_countries_profit):
    ax.text(v + 0.02 * v, i, format_thousands(v), ha='left', va='center')

ax.set_xlim(0, max(top_10_countries_profit) * 1.15)

plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/7cf17f24-3c05-43b4-a4f6-65cb2225c198)

---

## 5. Customer Purchase Frequency

```python
customer_frequency = df['customer_name'].value_counts()

plt.hist(customer_frequency, bins=30, color='skyblue', alpha=0.7)

# Median, Q1, Q3
median = np.percentile(customer_frequency, 50)
q1 = np.percentile(customer_frequency, 25)
q3 = np.percentile(customer_frequency, 75)

# mode_value is the value that shows up ex:'68'| mode_count is how often that value shows up ex: total count '68' appear is 30 times
mode_value = mode(customer_frequency)[0]
mode_count = mode(customer_frequency)[1]

# add line for median, Q1, Q3
plt.axvline(x=median, color='red', linestyle='--', linewidth=1.5, label='Median: {:.0f}'.format(median))
plt.axvline(x=q1, color='green', linestyle='--', linewidth=1.5, label='Q1: {:.0f}'.format(q1))
plt.axvline(x=q3, color='orange', linestyle='--', linewidth=1.5, label='Q3: {:.0f}'.format(q3))

# add line for mode
if mode_value >= plt.gca().get_xlim()[0] and mode_value <= plt.gca().get_xlim()[1]:
    plt.axvline(x=mode_value, color='purple', linestyle='--', linewidth=1.5, label='Mode: {:.0f} ({}x)'.format(mode_value, mode_count))
else:
    plt.text(mode_value, plt.gca().get_ylim()[1] * 0.6, 'Mode: {:.0f} ({} x)'.format(mode_value, mode_count), color='purple', ha='center', va='center')

plt.legend()

plt.xlabel('Purchase Frequency')
plt.ylabel('Total Customers')
plt.title('Customer Purchase Frequency')

plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/ef9fcc39-689e-4095-86ef-95c402c563d3)

---

## 6. Order Priority Distribution

```python
# Create Countplot
sns.countplot(x='order_priority', data=df, color='skyblue')

# Adding Numeric Value above bar
for p in plt.gca().patches:
    plt.gca().annotate('{:,.0f}'.format(p.get_height()), (p.get_x() + p.get_width() / 2., p.get_height()), 
                       ha='center', va='bottom', xytext=(0, 1), textcoords='offset points')

plt.title('Order Priority Distribution')
plt.xlabel('Order Priority')
plt.ylabel('Total Order')

plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/4561de56-c09f-4a1c-a21f-e7ae8f0a8738)

---

## 7. Correlation between Discount and Profit

```python
# Scatter plot between Discount and profit
sns.scatterplot(x='discount', y='profit', data=df, color='skyblue', alpha=0.8)

# Variable that count correlation coefficient between discount and profit
correlation_coefficient = df['discount'].corr(df['profit'])

# adding that correlation coefficient to the plot
plt.text(0.2, -2000, 'Correlation Coefficient: {:.2f}'.format(correlation_coefficient), fontsize=10, color='red')

plt.xlabel('Discount (%)')
plt.ylabel('Profit')
plt.title('Correlation between Discount and Profit')

plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/6898a01f-67c7-486f-b894-d1bcd3e3cb57)

---

## 8. Monthly Profit(Discount Apply)

```python
def format_thousands(x):
    return '{:.1f}K'.format(x / 1000)

df['order_date'] = pd.to_datetime(df['order_date'])

df['year'] = df['order_date'].dt.year
df['month'] = df['order_date'].dt.month

monthly_profit = df.groupby(['year', 'month'])['profit'].sum()

fig, axes = plt.subplots(2, 2, figsize=(15, 10))

# Loop through each subplot axis and corresponding year from 2011 to 2014
for ax, year in zip(axes.flatten(), range(2011, 2015)):
    data = monthly_profit.loc[year]
    ax.plot(data.index, data.values, marker='o', linestyle='-', alpha=0.5)
    ax.set_title('Monthly Profit by Year {}'.format(year))
    ax.set_xlabel('Months')
    ax.set_ylabel('Profit')
    
    for i, v in zip(data.index, data.values):
        ax.text(i, v * 1.02, format_thousands(v), ha='center', va='bottom')

    ax.set_ylim(0, max(data.values) * 1.08)

# adding legends
axes[0, 0].legend(['Profit'], loc='upper left')
axes[0, 1].legend(['Profit'], loc='upper left')
axes[1, 0].legend(['Profit'], loc='upper left')
axes[1, 1].legend(['Profit'], loc='upper left')

plt.tight_layout()
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/423eb2eb-4f7e-4136-a12c-b6eb7eca0257)

---

## 9. Average Profit(Discount Apply) per Order

```python
# Calculating Descriptive Statistics profit per Order
order_income_stats = df.groupby('order_id')['profit'].sum().describe()

# Calculating IQR
Q1 = order_income_stats['25%']
Q3 = order_income_stats['75%']
IQR = Q3 - Q1

# Defining the upper and lower bounds without outliers
lower_bound = Q1 - 1.5 * IQR
upper_bound = Q3 + 1.5 * IQR
avg_profit_order_no_outliers = df.groupby('order_id')['profit'].sum().loc[(df.groupby('order_id')['profit'].sum() >= lower_bound) & (df.groupby('order_id')['profit'].sum() <= upper_bound)]
avg_profit_order_no_outliers.describe()
```

### Output :

| Statistic | Value        |
|-----------|--------------|
| Count     | 20500.000000 |
| Mean      | 32.443220    |
| Std       | 62.547835    |
| Min       | -133.548000  |
| 25%       | 1.500000     |
| 50%       | 17.252400    |
| 75%       | 59.400000    |
| Max       | 222.740000   |

```python

plt.figure(figsize=(10, 6))
avg_profit_order_no_outliers.hist(bins=30, color='skyblue', edgecolor='black')
plt.xlabel('Profit per Order')
plt.ylabel('Total Order')
plt.title('Profit per Order Distribution without Outliers')

plt.text(0.5, 0.95, f"Count: {avg_profit_order_no_outliers.count()}", transform=plt.gca().transAxes)
plt.text(0.5, 0.9, f"Mean: {avg_profit_order_no_outliers.mean():.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.85, f"Std: {avg_profit_order_no_outliers.std():.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.8, f"Min: {avg_profit_order_no_outliers.min():.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.75, f"25%: {avg_profit_order_no_outliers.quantile(0.25):.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.7, f"50%: {avg_profit_order_no_outliers.quantile(0.50):.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.65, f"75%: {avg_profit_order_no_outliers.quantile(0.75):.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.6, f"Max: {avg_profit_order_no_outliers.max():.2f}", transform=plt.gca().transAxes)

plt.grid(False)
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/c1ec955b-6050-4d34-8332-ab78932036c0)

---

## 10. RFM Analysis

```python
latest_date = df['order_date'].max()

# Calculating Recency, Frequency, and Monetary values
rfm_table = df.groupby('customer_name').agg({
    'order_date': lambda x: (latest_date - x.max()).days,
    'order_id': 'count',
    'profit': 'sum'
})

# Renaming columns to Recency, Frequency, and Monetary
rfm_table.rename(columns={
    'order_date': 'Recency',
    'order_id': 'Frequency',
    'profit': 'Monetary'
}, inplace=True)

# Normalization of RFM values
rfm_table['Recency'] = (rfm_table['Recency'] - rfm_table['Recency'].min()) / (rfm_table['Recency'].max() - rfm_table['Recency'].min())
rfm_table['Frequency'] = (rfm_table['Frequency'] - rfm_table['Frequency'].min()) / (rfm_table['Frequency'].max() - rfm_table['Frequency'].min())
rfm_table['Monetary'] = (rfm_table['Monetary'] - rfm_table['Monetary'].min()) / (rfm_table['Monetary'].max() - rfm_table['Monetary'].min())

# Assigning RFM scores
rfm_table['R_Score'] = pd.qcut(rfm_table['Recency'], 4, ['1', '2', '3', '4'])
rfm_table['F_Score'] = pd.qcut(rfm_table['Frequency'], 4, ['4', '3', '2', '1'])
rfm_table['M_Score'] = pd.qcut(rfm_table['Monetary'], 4, ['4', '3', '2', '1'])

# Combining scores into one column
rfm_table['RFM_Score'] = rfm_table['R_Score'].astype(str) + rfm_table['F_Score'].astype(str) + rfm_table['M_Score'].astype(str)
rfm_table.sample(5)
```

### Output :

| customer_name   | Recency  | Frequency | Monetary | R_Score | F_Score | M_Score | RFM_Score |
|-----------------|----------|-----------|----------|---------|---------|---------|-----------|
| Tamara Manning | 0.149533 | 0.329114  | 0.545024 | 4       | 4       | 2       | 442       |
| Susan Gilcrest | 0.037383 | 0.367089  | 0.451475 | 2       | 3       | 4       | 234       |
| Andy Reiter    | 0.014019 | 0.075949  | 0.626710 | 1       | 4       | 1       | 141       |
| Brian Moss     | 0.077103 | 0.620253  | 0.710812 | 3       | 1       | 1       | 311       |
| Joseph Airdo   | 0.000000 | 0.594937  | 0.471780 | 1       | 1       | 4       | 114       |

```python
plt.figure(figsize=(14, 18))

# Scatter plot for Recency and Frequency
plt.subplot(3, 1, 1)
sns.scatterplot(x='Recency', y='Frequency', size='Monetary', sizes=(20, 200), hue='Monetary', data=rfm_table, palette='viridis', legend=False)
plt.title('Recency vs Frequency')
plt.xlabel('Recency')
plt.ylabel('Frequency')

# Scatter plot for Frequency and Monetary
plt.subplot(3, 1, 2)
sns.scatterplot(x='Frequency', y='Monetary', size='Recency', sizes=(20, 200), hue='Recency', data=rfm_table, palette='viridis', legend=False)
plt.title('Frequency vs Monetary')
plt.xlabel('Frequency')
plt.ylabel('Monetary')

# Scatter plot for Recency and Monetary
plt.subplot(3, 1, 3)
sns.scatterplot(x='Recency', y='Monetary', size='Frequency', sizes=(20, 200), hue='Frequency', data=rfm_table, palette='viridis', legend=False)
plt.title('Recency vs Monetary')
plt.xlabel('Recency')
plt.ylabel('Monetary')

plt.tight_layout()
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/8384fad1-4831-49f1-ab33-5c560dc6ca6d)

---

## 11. Sales Distribution by Customer Segment
This section provides an overview of the distribution of sales revenue across different customer segments.

```python
sales_by_segment = df.groupby('segment')['sales'].sum().reset_index()
sales_numeric = sales_by_segment['sales'].copy()
# format without scientific notation or commas
sales_by_segment['sales'] = sales_by_segment['sales'].apply(lambda x: f'${x:,.0f}')
print(sales_by_segment)
```

### Output : 

| segment      | sales        |
|--------------|--------------|
| Consumer     | $6,507,949   |
| Corporate    | $3,824,698   |
| Home Office  | $2,309,855   |

```python
segments = sales_by_segment['segment']

# Color for each segment
colors = ['green', 'skyblue', 'orange']
plt.figure(figsize=(10, 7))

# Function to display percentage and absolute values
def autopct_format(values):
    def my_format(pct):
        total = sum(values)
        val = int(round(pct*total/100.0))
        return f'{pct:.1f}%\n(${val:,.0f})'
    return my_format

plt.pie(sales_numeric, labels=segments, autopct=autopct_format(sales_numeric), startangle=140, colors=colors, shadow=True, explode=(0.05, 0, 0))
plt.title('Sales by Segment', fontsize=16)
plt.legend(segments, title="Segments", loc="center left", bbox_to_anchor=(1, 0, 0.5, 1))
plt.axis('equal')

plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/b4ee7cf7-9aeb-4ff3-a601-5444b7a3692e)

---

# Findings and business solution

## 1. Annual Sales and Profit Trend

Sales Data:
- 2011: $2,259,451
- 2012: $2,677,439
- 2013: $3,405,746
- 2014: $4,299,866

Profit Data:
- 2011: $248,941
- 2012: $307,415
- 2013: $408,513
- 2014: $504,166

### CAGR(Compound Annual Growth Rate) Sales
- CAGR = (Vf / Vi)^(1/n) - 1
- CAGR = (4,299,866 / 2,259,451)^(1/3) - 1
- CAGR ≈ (1.902)^(1/3) - 1
- CAGR ≈ 1.227 - 1
- CAGR ≈ 0.227
- CAGR ≈ 22.7%

### CAGR(Compound Annual Growth Rate) Profit
- CAGR = (Vf / Vi)^(1/n) - 1
- CAGR = (504,166 / 248,941)^(1/3) - 1
- CAGR ≈ (2.025)^(1/3) - 1
- CAGR ≈ 1.259 - 1
- CAGR ≈ 0.259
- CAGR ≈ 25.9%

### Summary
- CAGR Sales (2011-2014): 22.7%
- CAGR Profit (2011-2014): 25.9%

## Business Solutions
The analysis of Compound Annual Growth Rate (CAGR) for both sales and profit from 2011 to 2014 indicates significant growth rates. Here are some potential business solutions based on these trends:
- Sales Growth Strategy : Capitalize on the strong sales growth trend by expanding market reach through targeted marketing campaigns, exploring new customer segments, and enhancing product offerings to meet evolving consumer needs.
- Risk Management : Although the CAGR demonstrates positive growth, it's essential to assess and mitigate any associated risks. Conduct thorough market analyses, monitor industry trends, and develop contingency plans to address potential challenges such as market saturation, competitive pressures, or economic downturns.

---

## 2. Sales by Product Category

Sales by Product Category:
- Technology: $4,744,557
- Furniture: $4,110,874
- Office Supplies: $3,787,070

TOP 5 Products - Technology:
1. Canon ImageCLASS 2200 = $62K
2. Nokia Smart Phone = $72K
3. Motorola Smartphone = $73K
4. Cisco Smart Phone = $76K
5. Apple Smart Phone = $87K

TOP 5 Products - Furniture:
1. Novimex Executive Leather = $41K
2. SAFCO Executive Leather = $42K
3. Harbour Creations Executive = $50K
4. Office Star Executive = $51K
5. Hon Executive Leather = $58K

TOP 5 Products - Office Supplies:
1. Smead Lockers = $29K
2. Rogers File Cart = $29K
3. Hoover Stove, Red = $32K
4. Hoover Stove, White = $33K
5. Eldon File Cart = $34K

## Business Solutions

### Enhance Marketing for High-Demand Technology Products
- Increase Advertising Efforts: Launch targeted marketing campaigns emphasizing the latest features and benefits of top-selling technology products like Apple, Cisco, and Motorola smartphones.
- Bundling Offers: Create attractive bundles combining popular smartphones with accessories (e.g., headphones, cases) to increase the average transaction value.
- Leverage Social Media and Influencers: Utilize social media platforms and tech influencers to promote these products, capitalizing on the tech-savvy consumer base.

### Expand Product Range in Furniture and Office Supplies
- Product Diversification: Introduce new products within these categories to meet diverse customer needs. For Furniture, consider adding ergonomic chairs and standing desks. For Office Supplies, explore innovative organizational tools and eco-friendly products.
- Customer Feedback: Conduct surveys and focus groups to understand customer preferences and gaps in the current product range. Use this feedback to inform new product development.
- Seasonal Promotions: Run seasonal promotions and discounts on high-performing items like executive leather chairs and file carts to boost sales during peak shopping periods.

### Optimize Inventory and Supply Chain Management
- Data-Driven Inventory Management: Use sales data to forecast demand accurately and optimize inventory levels, ensuring popular products are always in stock.
- Supplier Relationships: Strengthen relationships with key suppliers to ensure timely restocking of high-demand items and negotiate better terms for bulk purchases.
- Supply Chain Efficiency: Implement advanced supply chain technologies to streamline logistics, reduce lead times, and minimize stockouts or overstock situations.

---

## 3. Distribution of Shipping Modes

Distribution of Shipping Modes:
- Standard Class: 30,775 shipments
- Second Class: 10,309 shipments
- Same Day: 2,701 shipments
- First Class: 7,505 shipments

## Insights
- Dominance of Standard Class: Most shipments (30,775) use Standard Class, indicating a preference for economical shipping.
- Limited Use of Same Day Shipping: Same Day shipping is the least utilized mode with only 2,701 shipments, suggesting lower demand or higher costs.
- Moderate Preference for Premium Shipping: First Class and Second Class shipping have moderate usage (7,505 and 10,309 shipments respectively), indicating a willingness to pay for faster delivery among some customers.

## Business Solutions

### Optimize Standard Class Shipping
- Negotiate Bulk Contracts: Reduce costs through bulk shipping contracts with logistics providers.
- Improve Processes: Enhance warehouse and order processing efficiency to speed up Standard Class shipping.
- Clear Communication: Set clear expectations about Standard Class delivery times to maintain customer satisfaction.

### Promote Faster Shipping Options
- Incentives: Offer discounts or promotions to encourage upgrades to faster shipping options.
- Loyalty Integration: Include premium shipping benefits in customer loyalty programs.
- Marketing Benefits: Highlight the advantages of faster shipping to attract more customers.

### Expand and Market Same Day Shipping
- Expand Coverage: Increase Same Day shipping availability in more regions, particularly urban areas.
- Targeted Campaigns: Use marketing to promote the convenience of Same Day shipping for urgent needs.
- Optimize Costs: Partner with local delivery services and improve route planning to manage costs effectively.

---

## 4. Income by Country/Region

Findings 
Income by Country/Region
- United States: $286,397
- China: $150,683
- India: $129,072
- United Kingdom: $111,900
- France: $109,029
- Germany: $107,323
- Australia: $105,485
- Mexico: $102,818
- Spain: $54,390
- El Salvador: $42,023

## Insights
- Revenue Distribution: The United States leads in income, followed by China and India, reflecting their economic strength and market size.
- European Presence: European countries like the United Kingdom, France, Germany, and Spain also contribute significantly to income, indicating a strong market presence in the region.
- Emerging Markets: Countries like India, China, and Mexico represent emerging markets with substantial income contributions, highlighting opportunities for further growth and expansion.

## Business Solutions

### Market Penetration and Expansion
- Strategic Investments: Allocate resources to penetrate and expand in high-income markets like the United States and Europe.
- Localized Strategies: Develop localized marketing and product strategies tailored to the preferences and trends of each country or region.
- Partnerships and Alliances: Form partnerships or alliances with local businesses or distributors to enhance market penetration and brand visibility.

### Focus on Emerging Markets
- Market Research: Conduct in-depth market research to understand the dynamics and opportunities in emerging markets like India, China, and Mexico.
- Adaptation: Adapt products, pricing, and distribution strategies to suit the unique needs and preferences of consumers in these markets.
- Investment in Infrastructure: Invest in building distribution networks and infrastructure to support operations and sales growth in emerging markets.

---

## 5. Customer Purchase Frequency

Findings Customer Purchase Frequency
- Median: 64
- Q1 (First Quartile): 55
- Q3 (Third Quartile): 74
- Mode: 68

## Insights
- Central Tendency: The median purchase frequency of 64 suggests that half of the customers make purchases more frequently than this value, while the other half makes purchases less frequently.
- Variability: The interquartile range (Q3-Q1) of 19 indicates the spread of purchase frequency values between the 25th and 75th percentiles, showing moderate variability.
- Common Frequency: The mode of 68 indicates that the most common purchase frequency among customers is 68, implying a concentration of customers around this value.

## Business Solutions

### Personalized Marketing Campaigns
- Segmentation: Segment customers based on their purchase frequency to tailor marketing campaigns according to their buying habits.
- Targeted Offers: Offer special promotions or discounts to incentivize customers whose purchase frequency falls below the median to increase their frequency.
- Retention Strategies: Implement customer retention strategies to encourage frequent buyers to maintain their purchasing habits and prevent attrition.

### Feedback and Engagement
- Customer Feedback: Solicit feedback from customers to understand factors influencing their purchase frequency and preferences.
- Engagement Initiatives: Engage customers through loyalty programs, interactive content, or community-building activities to foster brand loyalty and encourage repeat purchases.
- Continuous Monitoring: Continuously monitor customer purchase behavior and adapt strategies accordingly to maintain optimal purchase frequency levels and drive long-term customer satisfaction and loyalty.

---

## 6.  Order Priority Distribution

Findings Order Priority Distribution
- Medium: 29,433
- High: 15,501
- Critical: 3,932
- Low: 2,424

## Insights
- Priority Levels: Orders are distributed across multiple priority levels, ranging from Low to Critical, indicating varying degrees of urgency and importance.
- Prevalence of Medium Priority: Medium priority orders constitute the majority, suggesting that a significant portion of orders requires prompt attention but may not be urgent.
- Critical Orders: While Critical orders have the lowest count, their presence highlights the importance of addressing urgent customer needs promptly.

## Business Solutions

### Workflow Optimization
- Priority-Based Workflow: Implement priority-based workflow systems to streamline order processing, ensuring that higher priority orders are expedited while maintaining efficiency for lower priority orders.
- Automation: Utilize automation technologies to prioritize and route orders based on their priority level, reducing manual processing time and enhancing accuracy.

### Customer Communication
- Transparency: Communicate order priority status clearly to customers, setting realistic expectations for delivery times and response times based on the order priority.
- Proactive Notifications: Implement proactive notification systems to update customers on the status of their orders, particularly for Critical orders, to provide reassurance and maintain customer satisfaction.

---

## 7. Correlation between Discount and Profit
Correlation between Discount and Profit
- Correlation Coefficient: -0.32

## Insights
- Negative Correlation: The correlation coefficient of -0.32 indicates a negative correlation between discount and profit. This suggests that as the discount increases, the profit tends to decrease, and vice versa.
- Directional Relationship: The negative correlation implies an inverse relationship between discount and profit. This means that offering higher discounts may lead to lower profits, while reducing discounts or increasing prices may result in higher profits.

## Business Solutions

### Targeted Discounting
- Segmentation: Segment customers based on purchasing behavior, preferences, and price sensitivity to offer targeted discounts to high-value customers while minimizing discounts for low-margin segments.
- Promotional Bundles: Offer discounts as part of bundled promotions or loyalty programs to incentivize additional purchases and mitigate the impact of individual discounting on profit margins.

--- 

## 8. Monthly Profit(Discount Apply)

Year 2011:
- January: $8.3K
- June: $23.4K
- July: $5.6K
- September: $35.8K
- December: $40.6K

Year 2012:
- January: $10.4K
- June: $34.4K
- July: $15.6K
- August: $43.6K
- December: $33K

Year 2013:
- January: $26.8K
- June: $45.5K
- July: $28.9K
- December: $50.2K

Year 2014:
- January: $28K
- June: $43.8K
- July: $28K
- September: $68K
- December: $46.9K

## Insights
- Seasonal Variations: Profit fluctuates throughout the year, with certain months experiencing higher peaks and others lower troughs across all years.
- Trend Analysis: Overall, there is an upward trend in profit over the years, despite fluctuations in individual months.
- Yearly Patterns: Each year exhibits similar patterns of profit fluctuations, with some months consistently performing better than others.

## Business Solutions

### Seasonal Promotions
- Targeted Campaigns: Launch seasonal promotions and marketing campaigns during peak months to capitalize on increased consumer spending and maximize profitability.
- Inventory Management: Anticipate demand fluctuations and adjust inventory levels accordingly to ensure sufficient stock during peak periods while minimizing excess inventory during slower months.

### Cost Optimization
- Expense Review: Conduct a comprehensive review of expenses and identify opportunities for cost optimization to maintain profitability during slower months.
- Supplier Negotiations: Negotiate favorable terms with suppliers to reduce procurement costs and improve margins, especially during periods of lower profitability.

---

## 9. Average Profit(Discount Apply) per Order
- Count: 20,500 orders
- Mean: $32 (rounded)
- Standard Deviation: $63 (rounded)
- Minimum: -$134
- 25th Percentile (Q1): $2
- Median (50th Percentile): $17
- 75th Percentile (Q3): $59
- Maximum: $223

## Insights
- Average Profit: The average profit per order, considering discounts, is approximately $32.
- Variability: The standard deviation of approximately $63 suggests a considerable variation in profit values around the mean.
- Distribution: The data is positively skewed, with outliers on the higher end of the profit spectrum.

## Business Solutions

### Profitability Analysis
- Segment Analysis: Utilize data analytics to identify high-profit customer segments or product categories and allocate resources accordingly.
- Product Mix Optimization: Analyze profitability data to optimize the product mix, focusing on high-margin products to increase overall profitability.
### Cost Management
- Cost Reduction Strategies: Implement cost reduction strategies based on data-driven insights, such as streamlining operations and negotiating supplier contracts to improve profit margins.

---

## 10. Sales Distribution by Customer Segment
- Consumer: $6,507,949
- Corporate: $3,824,698
- Home Office: $2,309,855

## Insights
- Consumer Segment Dominance: Consumer segment accounts for the highest sales volume, indicating a significant portion of revenue comes from individual customers.
- Corporate Segment Contribution: Corporate segment contributes substantially to sales, suggesting strong business-to-business sales performance.
- Home Office Segment: While the Home Office segment contributes the least to sales, it still represents a notable portion of revenue, highlighting the importance of catering to small office and home office customers.

## Business Solutions

### Targeted Marketing Strategies
- Segment-Specific Campaigns: Develop targeted marketing campaigns tailored to each customer segment to effectively communicate product value propositions and enhance sales performance.
- Personalization: Utilize customer data to personalize marketing messages and offers for each segment, increasing relevance and engagement.

### Product Assortment Optimization
- Segment-Specific Products: Optimize product assortment to meet the unique needs and preferences of each customer segment, ensuring a diverse range of offerings tailored to different customer demographics.
- Product Bundling: Create bundled product packages tailored to each segment's preferences to encourage higher order values and enhance customer satisfaction.

---

