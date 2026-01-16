## SQL-Mastery-Series
# My journey of being Pro in SQL

# 1. SQL Basics-- Data Retrival- (Single Table)

# a) SELECT
The SELECT statement is used to retrieve and display data from one or more tables in a structured and readable format.
# i) Select All column
SELECT * from table;
Used to retrive all column for the respective table

why to avoid select * in the projects?
➡ Performance
➡ Memory
➡ Readability

# ii) Select Multiple Columns
SELECT col1, col2,col3 from table;
Here we fectch col1, col2, col3 from the respective table

# iii) Using Column Aliases
Used to change/ Rename the column in output.
For example Select name as student_name, age as student_age from student;
Used to make results redable.

# iv) SELECT Statement with WHERE Clause
It is used when we want to see table values with specific conditions
Example :- Filter students whose age is 18 years old
SELECT student_name from students where age == 18;

# iv) SELECT with GROUP BY Clause
GROUP BY is used to group rows that have the same values in a column and apply aggregate functions on each group.
Aggregate Functions (Used with GROUP BY)
| Function  | Purpose        |
| --------- | -------------- |
| `COUNT()` | Number of rows |
| `SUM()`   | Total          |
| `AVG()`   | Average        |
| `MIN()`   | Minimum        |
| `MAX()`   | Maximum        |

Example 1:- query to returns the number of students in each department by grouping the students table department-wise.

SELECT department, COUNT(*) AS total_students
FROM students
GROUP BY department;

# v) SELECT Statement with HAVING Clause
The HAVING clause is used to filter results after applying GROUP BY.

Select department, count (*) as total_students
From students 
group by department
having count (*) > 30;

Explanation of above example:-
Groups students by department
Counts students in each department
Shows only departments with more than 30 students


| WHERE                          | HAVING                 |
| ------------------------------ | ------------------------ |
| Filters rows                   | Filters groups           |
| Used before GROUP BY           | Used after GROUP BY      |
| Cannot use aggregate functions | Uses aggregate functions |


# vi)  SELECT Statement with ORDER BY clause
ORDER BY is used to sort the result set of a query.

📌 Sorting happens after data is selected
📌 Default sorting order is ASC (ascending)

Example 1:- Students sorted by city and marks
select * from students
order by city asc, marks desc;


Example 2:- Departments with highest number of students
select department , count(*) as total
from student
group by department
order by total dsc;

# vi)  SELECT Statement with Limit
LIMIT is used to restrict the number of rows returned by a query.
Example:-
SELECT *
FROM students
LIMIT 5;



# Execution Order
FROM
WHERE
GROUP BY
HAVING
SELECT
ORDER BY
LIMIT









