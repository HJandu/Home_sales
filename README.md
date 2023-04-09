# <ins>Home Sales</ins>

Module 22 Big Data / SparkSQL

To view the final code [click here](https://github.com/HJandu/Home_sales/blob/main/Home_Sales.ipynb)

## Overview

In this challenge, I will use my knowledge of SparkSQL to determine key metrics about home sales data. Then I will use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## Before starting the challenge

* Import the necessary PySpark SQL functions for this challenge.

![Screen Shot 2023-04-09 at 01 29 37](https://user-images.githubusercontent.com/116304118/230748439-09fd3556-fb9e-4925-b52f-d18140e7cc7b.png)

* Read the home_sales_revised.csv data in the `Home_Sales.ipynb` into a Spark DataFrame.

![Screen Shot 2023-04-09 at 01 29 48](https://user-images.githubusercontent.com/116304118/230748519-a25bda31-2293-4c38-91ec-04c89219adb9.png)

* Create a temporary table called home_sales.

![Screen Shot 2023-04-09 at 01 45 01](https://user-images.githubusercontent.com/116304118/230748552-ac1cf122-76e4-402b-9667-5cf7eb6dbd62.png)

## Answering questions using SparkSQL

1. What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

![Screen Shot 2023-04-09 at 01 48 28](https://user-images.githubusercontent.com/116304118/230748634-22e224f2-6c15-43af-8b6f-6df9f934a043.png)

2. What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

![Screen Shot 2023-04-09 at 01 49 42](https://user-images.githubusercontent.com/116304118/230748659-365fe8da-6095-4445-92e6-4256502baba6.png)


3. What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

![Screen Shot 2023-04-09 at 01 50 29](https://user-images.githubusercontent.com/116304118/230748665-203574ea-e876-4d3f-9ad1-627fa24e3cfd.png)

4. What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

![Screen Shot 2023-04-09 at 01 51 04](https://user-images.githubusercontent.com/116304118/230748675-4898d07d-5e83-4cea-8e09-207910072f90.png)


#### Cache my temporary table home_sales and check if my temporary table is cached.

![Screen Shot 2023-04-09 at 01 31 16](https://user-images.githubusercontent.com/116304118/230748759-b7ffc3a5-eb4a-4638-9a60-a0189ba07639.png)

I Used the cached data to run the query that filters out the view ratings with an average price of greater than or equal to $350,000. I also determined the runtime and compare it to the uncached runtime.

--- 0.3426980972290039 seconds ---

The home sales dataset was partitioned by the "date_built" field on the formatted parquet home sales data. I then created a temporary table for the parquet data. After this, I ran the query that filters out the view ratings with an average price of greater than or equal to $350,000. The runtimewas determinded and compared to the uncached runtime.

--- 0.3578789234161377 seconds ---

#### Uncache the home_sales temporary table and verify that the home_sales temporary table is uncached using PySpark.

![Screen Shot 2023-04-09 at 01 31 31](https://user-images.githubusercontent.com/116304118/230748960-5f5b12a7-8acd-4607-976e-df3165cc973e.png)



