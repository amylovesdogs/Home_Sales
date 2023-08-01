# Home_Sales - SparkSQL and Colab
DU Data Analysis Module 22 Big Data Challenge<br>
Using SparkSQL to determine key metrics about home sales data.

## Queries
*Home_Sales_colab.ipynb* uses a SparkSQL home sales database created from the
from the file *home_sales_revised.csv*. The code does the following queries:
1. What is the average price for a four bedroom house sold in each year rounded to two decimal places?
2. What is the average price of a home for each year the home was built that have 3 bedrooms and 3 bathrooms rounded to two decimal places?
3. What is the average price of a home for each year built that have 3 bedrooms, 3 bathrooms, with two floors and are greater than or equal to 2,000 square feet rounded to two decimal places?
4. What is the average price of a home, for each view rating, rounded to two decimal places, where the homes are greater than or equal to $350,000? Note that I reworded this query after getting some help from AskBCS. The original assignment wording was unclear to me.

## Performance

The last query above (#4) was run the following ways and got the associated performance result. The database has 33,287 rows.
| Method                                | Performance   |
| ------------------------------------- | ------------- |
| No performance enhancements           | 1.22 seconds  |
| Caching the table                     | 0.76 seconds  |
| Parquet partion on date_built field   | 0.58 seconds  |
