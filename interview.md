💬 Interview Questions & Answers

1. How do you group data by month and year?
You can use the YEAR() and MONTH() functions on the date column and then group the results using GROUP BY YEAR(order_date), MONTH(order_date). This lets you summarize data month-wise across years.

2. What's the difference between COUNT(*) and COUNT(DISTINCT col)?
COUNT(*) counts all rows including duplicates and NULLs.
COUNT(DISTINCT col) counts only the unique non-null values in that specific column.

3. How do you calculate monthly revenue?
Multiply quantity by price to get revenue per row, then sum that using SUM(quantity * price), and group by MONTH(order_date) to get monthly totals.

4. What are aggregate functions in SQL?
Aggregate functions process multiple rows and return a single summarized value. Common examples are:

SUM() for total

COUNT() for number of rows

AVG() for average

MAX() and MIN() for highest/lowest values
They are usually used with GROUP BY to analyze grouped data.

5. How to handle NULLs in aggregates?
Most SQL aggregate functions ignore NULLs by default, except COUNT(*), which includes them.
To handle or replace NULL values before aggregation, use functions like IFNULL() or COALESCE() to convert them to zeros or default values.

6. What’s the role of ORDER BY and GROUP BY?
GROUP BY is used to group rows that have the same values in specified columns, often combined with aggregate functions.
ORDER BY is used to sort the final result set by one or more columns in ascending or descending order.

7. How do you get the top 3 months by sales?
First group the data by month and calculate total sales using SUM(quantity * price). Then sort it in descending order using ORDER BY and limit the results to 3 using LIMIT 3 to get the top 3 months.
