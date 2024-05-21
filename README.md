# Project Overview
this project revolves around exploring and analyzing a dataset to derive meaningful insights and inform decision-making. The primary focus is on understanding the data, performing various analyses, and visualizing the findings to communicate key observations effectively.

# About this Project
The project centers on a comprehensive analysis of a dataset encompassing various aspects such as sales, customer information, product details, and market segments. Key tasks undertaken include data validation, exploratory data analysis (EDA), statistical analysis, and visualization of trends and patterns within the dataset.

# Objective
The main objective of this project is to extract actionable insights from the dataset to drive business decisions and strategies. Through rigorous analysis and visualization, the aim is to uncover trends, identify opportunities, and address challenges within the data.

# User Story
As a data analyst, I meticulously validated the dataset to ensure data quality and integrity. This involved checking for missing values, duplicates, descriptive statistics, and ensuring proper data formats. By leveraging advanced analytical techniques, I aimed to uncover hidden patterns and correlations that could guide strategic decision-making.

# Additional Sections
- Data Validation: Detail the steps taken to validate the dataset, including checking for missing values, duplicates, descriptive statistics and ensuring proper data formats.
- Exploratory Data Analysis (EDA): Provide insights from the initial exploration of the dataset, including summary statistics, distributions, and correlations between variables.
- Statistical Analysis: Discuss any statistical tests or analyses conducted to validate findings or test hypotheses within the dataset.
- Visualization: Showcase visualizations created to represent key insights and trends discovered during the analysis process.
- Key Findings: Summarize the most significant findings and insights derived from the analysis, highlighting actionable recommendations or areas for further investigation.
- Conclusion: Reflect on the overall analysis process, lessons learned, and the impact of insights on potential business outcomes.

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
