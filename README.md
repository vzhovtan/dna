
## Understanding Customer's DNA-Center ordering

The goals of this analysis are to:

*Understand how customer attributes influence a customer’s decision to order a DNA Center License, and predict the probability of a DNA Center license order for a holdout sample of customers (available in testing.csv)*

Prior to assessing the main goals above, it is needed to perform some data cleanup and exploratory data analysis.

### Data Description

To preserve the confidentiality of customer data, the data for this project are simulated. However, fields and values are created to be similar to real customer data.

####Data Set 1: training.csv

Field Descriptions:

ID Variable:

* cust - a simulated customer ID (does not link to any real customer data)
* segment - Enterprise or Commercial customer
* vertical - Industry (e.g. Financial Services, Manufacturing)
* sub_vertical - A more granular version of vertical (e.g. Discrete Manufacturing)
* country - The raw data includes 14 distinct country values (e.g. BRAZIL)
* bookings - total customer bookings (across all products) in FY2018

Outcome:

purchase - a TRUE/FALSE indicator of whether the customer purchased a DNA-Center License in FY2018

####Data Set 2: testing.csv

The testing.csv file contains a smaller holdout sample of all customers. For these customers, there is no information whether a DNA-Center license was purchased. The fields are exactly the same as in training.csv, except the outcome field (purchase), which is not included.

####Analysis Questions

The following questions should be answered in a Jupyter Notebook or an RMarkdown document.

```
* Q1: Load training.csv into Python or R
* Q2: Explore the categorical predictors (segment, vertical, sub_vertical, country) for data quality issues. Using your best judgment given the data and Field Descriptions, fix these data quality issues. Provide your code and a text summary of the data quality issues in the report.
* Q3: Using graphical analysis and/or numeric summaries, explore the relationship between the 5 predictors (segment, vertical, sub_vertical, country, and bookings) and the outcome of interest (purchase).
* Q4: Use a statistical modeling method or machine learning algorithm of your choice to estimate the effects of the predictors on the outcome. When choosing a modeling approach, select a model that will yield a probability of purchase (see Q5 below) rather than an approach that yields only a binary classification. Use output from your model to describe the effects of each predictor on purchase. Please use precise interpretations.
* Q5: Using your model or algorithm to estimate the probability of purchase for each customer in testing.csv. Write a .csv file with file that will be a CSV containing two columns. The first column will be the customer ID found in testing.csv. The second column should be named prob_dnac_purchase and be a value strictly between 0 and 1.
```