# Quantium Virtual Internship: Retail Strategy and Performance Analysis - Project Overview
- Examine transaction data to look for inconsistencies, missing data, find outliers, correctly identify category items and numeric data across the different tables.
- Examine customer data to check for similar issues in customer data, look for nulls and merge the transaction data and customer data to prepare for data analysis
- Analyze data and customer segments by defining the metrics and looking at total sales, driver of sales, such as where the highest sales are coming from, etc. We will find interesting insights and trends in the data.
- Deep dive into customer segments by defining recommendations from the aformentioned insights, determine which segments we should target, and if packet sizes and form and overall conclusion based on the analysis.
- Select control stores - explore data and define metrics for control store. Look at the drivers and look at them visually to see if they are suitable
- Assess each trial store - Look at each of the trial store and compare them to the control store to see if there are significant difference

## Code and resources used
**Python:** 3.7 <br/>
**Packages:** pandas, seaborn, numpy, mlxtend

## Data
*customer_transaction:*
- **LYLTY_CARD_NBR:** unique card number for a customer
- **LIFESTAGE:** customer age group
- **PREMIUM_CUSTOMER:** type of customer (premium, budget, mainstream)

*QVI_transaction_data:*
- **DATE:** date of transaction
- **STORE_NBR:** store number
- **LYLTY_CARD_NBR:** unique card number for a customer
- **TXN_ID:** transaction ID
- **PROD_NBR:** product number
- **PROD_NAME:** product name
- **PROD_QTY:** product quantity
- **TOT_SALES:** total sales

*QVI_data (cleaned data from Task 1):*
- **LYLTY_CARD_NBR:** unique card number for a customer
- **DATE:** date of transaction
- **STORE_NBR:** store number
- **TXN_ID:** transaction ID
- **PROD_NBR:** product number
- **PROD_NAME:** product name
- **PROD_QTY:** product quantity
- **TOT_SALES:** total sales
- **PACK_SIZE:** chip pack size
- **BRAND:** chip brand
- **LIFESTAGE:** customer age group
- **PREMIUM_CUSTOMER:** type of customer (premium, budget, mainstream)

## Data Cleaning and Preperation
- Change date column to datetime
- Parse brand and pack sizes
- Remove special characters in PROD_NAME
- Remove salsa brands from PROD_NAME
- Find for outliers
- Replace brand names for similar brands
- Show distributions for brands and pack size
- Combine transaction_data and customer_data
- Find for nulls

## EDA
Some questions that we will answer in this analysis:
- Who spends the most on chips (total sales), describing customers by lifestage and
how premium their general purchasing behaviour is
- How many customers are in each segment
- How many chips are bought per customer by segment
- What's the average chip price by customer segment
We could also ask our data team for more information. Examples are:
- The customer's total spend over the period and total spend for each transaction
to understand what proportion of their grocery spend is on chips
- Proportion of customers in each customer segment overall to compare against the
mix of customers who purchase chips

## Selecting Control Stores
We want to select a store that match trial stores similar to a store before Feb 2019 in terms of:
- Monthly overall sales revenue
- Monthly number of customers
- Monthly number of transactions per customer

## Trial Success
Compare control store and trial store to see if the trial created statistically significant differences in sales and number of customers.
