# E Commerce Furniture Analysis

# Project Overview
This project analyzes sales data from an e-commerce platform focusing on furniture products. The goal is to gain insights into sales performance, customer behavior, and product trends to inform business strategies.

## Dataset Description
The dataset contains various details about furniture sales, including:
- Product Title: The name of the product.
- Product Type: The category or type of furniture.
- Brand: The brand of the product.
- Quantity Sold: The number of units sold.
- Price: The selling price of the product.
- Original Price: The original price before any discounts.
- Cost of Shipping: The shipping cost, with 'Free shipping' as a common entry.
- Total Revenue: The total revenue generated from the sales.
- Discount: The amount of discount applied.
- Discount Percentage: The percentage discount applied.
- Gross Profit: Calculated as Total Revenue - (Original Price * Quantity Sold).
- Gross Profit Margin: Calculated as (Gross Profit / Total Revenue) * 100.
- Net Profit: Calculated as Total Revenue - (Original Price * Quantity Sold + 
  Cost of Shipping).
- Net Profit Margin: Calculated as (Net Profit / Total Revenue) * 100.
  
## Data Preprocessing
Steps taken to clean and prepare the data:
- Handling Missing Values: Ensured there are no missing values in crucial columns.
- Correcting Data Types: Converted string representations of numerical values to 
  appropriate data types.
- Parsing Shipping Costs: Converted 'Free shipping' to 0 and removed '+Shipping: 
  $' prefix to extract numerical values.
df['cost of shipping'] = df['cost of shipping'].str.replace('Free shipping', '0')
df['cost of shipping'] = df['cost of shipping'].str.replace(r'\+Shipping: \$', '', regex=True)
df['cost of shipping'] = df['cost of shipping'].str.replace(',', '')
df['cost of shipping'] = df['cost of shipping'].astype('float')
- Generating Additional Columns: Created columns for gross profit, gross profit 
  margin, net profit, and net profit margin.

## Exploratory Data Analysis
Key areas explored:
- Sales Distribution: Analysis of sales across different product types and brands 
  to identify popular categories and brands.
- Revenue Analysis: Examination of total revenue to determine high-performing 
  products.
- Profit Margins: Detailed analysis of gross and net profit margins to understand 
  profitability.
- Top-Selling Products: Identification of products with the highest sales volume 
  and revenue.

Tools used for EDA include pandas, matplotlib, and seaborn.

Key insights discovered:

- Certain product types and brands consistently perform better in terms of sales 
  and revenue.
- Products with higher discounts tend to have higher sales volumes.
- Shipping costs significantly impact net profit margins.

## Dashboard in Tableau
A comprehensive dashboard has been created in Tableau to visualize the key insights. The dashboard includes:

- Sales Performance Overview: Visualizations showing overall sales trends.
- Top Product and Brand Analysis: Insights into the best-performing products and 
  brands.
- Profit Margin Insights: Detailed views of gross and net profit margins.

https://public.tableau.com/views/EcommerceFurnitureDashboard/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## Conclusion and Future Work
This analysis provided valuable insights into the sales performance and customer preferences for furniture products. Key findings include:

- High-performing product categories and brands.
- The impact of discounts and shipping costs on sales and profitability.

Future work could include:

- Customer Segmentation: Analyzing customer data to identify distinct segments.
- Predictive Modeling: Building models to predict future sales trends.
- Impact Analysis: Evaluating the impact of different discount strategies on 
  sales.

# License

This project is licensed under the MIT License. See the LICENSE file for more details.

# Contact
For any questions or feedback, please contact:
Luis Olivero
luis.a.olivero94@gmail.com
