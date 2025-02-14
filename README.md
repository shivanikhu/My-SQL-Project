# My-SQL-Project
SQL Queries Used
SELECT: Extracted relevant data.
WHERE: Filtered records based on conditions.
LIKE: Searched for pattern matches.
JOIN: Combined data from multiple tables.
GROUP BY: Aggregated data for analysis.
HAVING: Filtered aggregated results.
ORDER BY: Sorted data.
Subqueries & CTEs: Used for complex queries.

Example Queries -
Filtering Sales Data-

SELECT product_name, total_sales
FROM sales
WHERE total_sales > 10000
ORDER BY total_sales DESC;

Finding Customers with a Specific Pattern:-

SELECT customer_name, email_id
FROM customers
WHERE email_id LIKE '%@gmail.com';


Joining Tables to get customer records:-

SELECT customers.customer_name, orders.order_id, orders.total_cost
FROM customers
JOIN orders ON 
customers.customer_id = orders.customer_id
WHERE orders.total_cost > 200;

 Aggregate Functions:
COUNT() – Counts the number of rows
SUM() – Calculates the total sum of a column
AVG() – Computes the average value of a column
MIN() – Finds the minimum value in a column
MAX() – Finds the maximum value in a column


Examples of Aggregate Functions in SQL:-
1. Using COUNT()
2. Counts  total number of employees in a table.

3. SELECT COUNT(*) AS total_employees FROM employees;

4.  Using SUM()
5.  Calculates the total salary paid to employees:
6.  SELECT SUM(salary) AS total_salary FROM employees;

7. Using AVG()
8. Find the average salary of employees.
9. SELECT AVG(salary) AS average_salary FROM employees;

10. Using MIN() and MAX()
11. Finds the lowest salaries.

12.  SELECT MIN(salary) AS lowest_salary
  
13.   Finds the highest salaries.

14. MAX(salary) AS highest_salary FROM employees;

15. Using Aggregate Functions with GROUP BY:-
16. Finds the total salary per department.


17. SELECT department, SUM(salary) AS total_salary
FROM employees
GROUP BY department;

 Using Aggregate Functions with HAVING:-
 Filtering groups based on aggregate function results (e.g., departments with total salary greater than 5,000)

 SELECT department, SUM(salary) AS total_salary
FROM employees
GROUP BY department
HAVING total_Salary > 5000;


 

