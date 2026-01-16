## SQL-Mastery-Series
# My journey of being Pro in SQL

# 1. SQL Basics-- Data Retrival- (Single Table)

# a) SELECT
The SELECT statement is used to retrieve and display data from one or more tables in a structured and readable format.
# i) Select All column
SELECT * from table;
Used to retrive all column for the respective table

why to avoid select * in the projects?
Why avoid SELECT *?
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




