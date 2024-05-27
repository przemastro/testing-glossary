### Easy Questions:
1. How do you retrieve all records from a table named Employees?

 > SELECT * FROM Employees;

2. How do you filter records in SQL Server using the WHERE clause?

 > SELECT * FROM Employees WHERE department = 'IT';

3. How do you retrieve distinct values from a column in SQL Server?

 > SELECT DISTINCT department FROM Employees;

4. How do you sort records in SQL Server?

 > SELECT * FROM Employees ORDER BY salary DESC;

5. How do you insert records into a table in SQL Server?

 > INSERT INTO Employees (name, department, salary) VALUES ('John Doe', 'IT', 50000);

6. How do you update records in SQL Server?

 > UPDATE Employees SET salary = 55000 WHERE name = 'John Doe';

7. How do you delete records from a table in SQL Server?

 > DELETE FROM Employees WHERE name = 'John Doe';

8. How do you count the number of records in a table in SQL Server?

 > SELECT COUNT(*) FROM Employees;

9. How do you find the maximum value in a column in SQL Server?

 > SELECT MAX(salary) FROM Employees;

10. How do you find the average value of a column in SQL Server?

 > SELECT AVG(salary) FROM Employees;

11. How do you rename a column in SQL Server?

 > EXEC sp_rename 'Employees.old_column_name', 'new_column_name', 'COLUMN';

12. How do you retrieve the current date and time in SQL Server?

 > SELECT GETDATE();

13. How do you concatenate two strings in SQL Server?

 > SELECT 'Hello' + ' ' + 'World';

14. How do you select the first 10 records from a table?

 > SELECT TOP 10 * FROM Employees;

15. How do you check if a table exists in SQL Server?

 > IF OBJECT_ID('Employees', 'U') IS NOT NULL
   PRINT 'Table exists';

16. How do you remove duplicates from a result set in SQL Server?

 > SELECT DISTINCT column_name FROM Employees;

17. How do you change the data type of a column in SQL Server?

 > ALTER TABLE Employees ALTER COLUMN salary DECIMAL(10,2);

18. How do you convert a string to uppercase in SQL Server?

 > SELECT UPPER('hello');

19. How do you find the length of a string in SQL Server?

 > SELECT LEN('hello');

20. How do you check the SQL Server version?

 > SELECT @@VERSION;

### Moderate Difficulty Questions:

1. How do you perform a join operation in SQL Server?

 > SELECT * FROM Employees e INNER JOIN Departments d ON e.department_id = d.id;

2. How do you use the GROUP BY clause in SQL Server?

 > SELECT department, AVG(salary) FROM Employees GROUP BY department;

3. How do you filter results based on multiple conditions using the AND and OR operators in SQL Server?

 > SELECT * FROM Employees WHERE department = 'IT' AND salary > 50000;

4. How do you use the LIKE operator in SQL Server?

 > SELECT * FROM Employees WHERE name LIKE 'John%';

5. How do you use the IN operator in SQL Server?

 > SELECT * FROM Employees WHERE department IN ('IT', 'HR');

6. How do you use the BETWEEN operator in SQL Server?

 > SELECT * FROM Employees WHERE salary BETWEEN 40000 AND 60000;

7. How do you use subqueries in SQL Server?

 > SELECT * FROM Employees WHERE department_id IN (SELECT id FROM Departments WHERE name = 'IT');

8. How do you create a new table in SQL Server?

 > CREATE TABLE NewTable (
id INT PRIMARY KEY,
name VARCHAR(255),
department VARCHAR(255),
salary DECIMAL(10,2)
);

9. How do you add a new column to an existing table in SQL Server?

 > ALTER TABLE Employees ADD COLUMN email VARCHAR(255);

10. How do you create an index on a column in SQL Server?

 > CREATE INDEX idx_department ON Employees(department);

11. How do you use the CASE statement in SQL Server?

 > SELECT name,
CASE
WHEN salary > 50000 THEN 'High'
WHEN salary BETWEEN 30000 AND 50000 THEN 'Medium'
ELSE 'Low'
END AS salary_level
FROM Employees;

12. How do you create a view in SQL Server?

 > CREATE VIEW EmployeeView AS
SELECT name, department, salary
FROM Employees;

13. How do you retrieve records using an alias in SQL Server?

 > SELECT e.name AS EmployeeName, d.name AS DepartmentName
FROM Employees e
JOIN Departments d ON e.department_id = d.id;

14. How do you get the first and last record from a table in SQL Server?

 > (SELECT TOP 1 * FROM Employees ORDER BY id ASC)
UNION ALL
(SELECT TOP 1 * FROM Employees ORDER BY id DESC);

15. How do you retrieve the nth highest salary from a table in SQL Server?

 > SELECT salary
FROM (SELECT salary,
ROW_NUMBER() OVER (ORDER BY salary DESC) AS RowNum
FROM Employees) AS Result
WHERE RowNum = 3;

16. How do you update data based on a condition from another table in SQL Server?

 > UPDATE e
SET e.salary = e.salary * 1.10
FROM Employees e
JOIN Departments d ON e.department_id = d.id
WHERE d.name = 'Sales';
 
17. How do you delete records that are duplicates in SQL Server?

 > WITH CTE AS (
SELECT name,
ROW_NUMBER() OVER (PARTITION BY name ORDER BY id) AS RowNum
FROM Employees
)
DELETE FROM CTE WHERE RowNum > 1;

18. How do you find the second highest value in a column in SQL Server?

 > SELECT MAX(salary) AS SecondHighestSalary
FROM Employees
WHERE salary < (SELECT MAX(salary) FROM Employees);

19. How do you perform a left join in SQL Server?

 > SELECT e.name, d.name
FROM Employees e
LEFT JOIN Departments d ON e.department_id = d.id;

20. How do you convert a date to a specific format in SQL Server?

 > SELECT FORMAT(GETDATE(), 'yyyy-MM-dd');

### Difficult Questions:
1. What are SQL Server system databases? Name them.

 - System databases in SQL Server include master, model, msdb, tempdb, and resource.

2. How do you handle NULL values in SQL Server?

 - NULL values can be handled using the IS NULL and IS NOT NULL operators in SQL Server.

3. How do you perform transactions in SQL Server?

 - Transactions in SQL Server are handled using the BEGIN TRANSACTION, COMMIT, and ROLLBACK statements.

4. How do you use window functions in SQL Server?

 - Window functions in SQL Server are used with the OVER clause to perform calculations across a set of rows.

5. How do you create stored procedures in SQL Server?

 > CREATE PROCEDURE GetEmployeeDetails
AS
BEGIN
SELECT * FROM Employees;
END;

6. How do you create user-defined functions in SQL Server?

 > CREATE FUNCTION dbo.GetEmployeeCount ()
RETURNS INT
AS
BEGIN
RETURN (SELECT COUNT(*) FROM Employees);
END;

7. How do you grant permissions to users in SQL Server?

 > GRANT SELECT ON Employees TO user1;

8. How do you implement error handling in SQL Server?

 - Error handling in SQL Server can be implemented using TRY...CATCH blocks.

9. How do you optimize SQL Server queries for better performance?

 - SQL Server queries can be optimized by creating appropriate indexes, avoiding table scans, and optimizing join operations.

10. How do you schedule jobs in SQL Server using SQL Server Agent?

 - Jobs in SQL Server can be scheduled using SQL Server Agent by creating a new job, defining the job steps, and scheduling the job to run at specific intervals.

11. How do you implement recursive queries in SQL Server?

 > WITH EmployeeHierarchy AS (
SELECT id, name, manager_id
FROM Employees
WHERE manager_id IS NULL
UNION ALL
SELECT e.id, e.name, e.manager_id
FROM Employees e
INNER JOIN EmployeeHierarchy eh ON e.manager_id = eh.id
)
SELECT * FROM EmployeeHierarchy;

12. How do you write a query to pivot data in SQL Server?

 > SELECT department, [2019], [2020], [2021]
FROM (SELECT department, year, salary FROM Employees) AS SourceTable
PIVOT (SUM(salary) FOR year IN ([2019], [2020], [2021])) AS PivotTable;

13. How do you write a query to unpivot data in SQL Server?

 > SELECT department, year, salary
FROM (SELECT department, [2019], [2020], [2021] FROM PivotTable) AS SourceTable
UNPIVOT (salary FOR year IN ([2019], [2020], [2021])) AS UnpivotTable;

14. How do you create a trigger in SQL Server?

 > CREATE TRIGGER trgAfterInsert ON Employees
AFTER INSERT
AS
BEGIN
INSERT INTO EmployeeAudit (employee_id, audit_action)
SELECT id, 'INSERT' FROM inserted;
END;

15. How do you handle complex string manipulation in SQL Server?

 > SELECT SUBSTRING('Hello World', 1, 5),
CHARINDEX('W', 'Hello World'),
REPLACE('Hello World', 'World', 'SQL');

16. How do you manage and use temp tables in SQL Server?

 > CREATE TABLE #TempTable (id INT, name VARCHAR(50));
INSERT INTO #TempTable VALUES (1, 'John'), (2, 'Jane');
SELECT * FROM #TempTable;
DROP TABLE #TempTable;

17. How do you create and use a common table expression (CTE) in SQL Server?

 > WITH SalesCTE AS (
SELECT department, SUM(salary) AS total_salary
FROM Employees
GROUP BY department
)
SELECT * FROM SalesCTE WHERE total_salary > 50000;

18. How do you write a query to merge data from two tables in SQL Server?

 > MERGE INTO Employees AS target
USING NewEmployees AS source
ON target.id = source.id
WHEN MATCHED THEN
UPDATE SET target.name = source.name, target.salary = source.salary
WHEN NOT MATCHED BY TARGET THEN
INSERT (id, name, salary) VALUES (source.id, source.name, source.salary)
WHEN NOT MATCHED BY SOURCE THEN
DELETE;

19. How do you perform error handling using TRY...CATCH in SQL Server?

 > BEGIN TRY
-- Generate a divide-by-zero error
SELECT 1 / 0;
END TRY
BEGIN CATCH
SELECT ERROR_MESSAGE() AS ErrorMessage;
END CATCH;

20. How do you design and implement partitioned tables in SQL Server?

 > -- Create a partition function
CREATE PARTITION FUNCTION myRangePF1 (int)
AS RANGE LEFT FOR VALUES (1, 100, 1000);

 > -- Create a partition scheme
CREATE PARTITION SCHEME myRangePS1
AS PARTITION myRangePF1
TO (group1, group2, group3, group4);

 > -- Create a partitioned table
CREATE TABLE Orders
(
OrderID int,
OrderDate datetime,
CustomerID int,
Amount money
) ON myRangePS1 (OrderID);