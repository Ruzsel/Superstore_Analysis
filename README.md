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
1. Annual Sales and Profit Trend : Observing the sales and profit trend from year to year.
2. Sales by Product Category : Identifying the most popular product category. and breakdown top 5 `product_name` from that category
3. Distribution of Shipping Modes : Observing how shipping modes are distributed.
4. Income by Country/Region : Identifying which country or region provides the highest income.
5. Customer Purchase Frequency : Understanding how often customers make purchases.
6. Order Priority Distribution : Observing how order priorities are distributed.
7. Correlation between Discount and Profit : Determining if there's a correlation between the amount of discount given and the profit earned.
8. Monthly Profit(Discount Apply) : Viewing profit per month for each year.
9. Average Profit(Discount Apply) per Order : Calculating the average profit obtained from each order without outliers.
10. RFM Analysis : Determining customer segmentation based on Recency, Frequency, and Monetary.

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
