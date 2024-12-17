## <b>INSERT INTO SELECT<b> statement copies data from one table and inserts it into another table.  

> The INSERT INTO SELECT statement requires that the data types in source and target tables match.  

Note: The existing records in the target table are unaffected.  

INSERT INTO SELECT Syntax

```
INSERT INTO table2
SELECT * FROM table1
WHERE condition;
```
#### 01. Copy "Suppliers" into "Customers" (the columns that are not filled with data, will contain NULL):
```
INSERT INTO Customers (CustomerName, City, Country)
SELECT SupplierName, City, Country FROM Suppliers;
```

## <b>The SELECT INTO statement<b> copies data from one table into a new table.

>SELECT INTO Syntax
>Copy all columns into a new table:
```
SELECT *
INTO newtable [IN externaldb]
FROM oldtable
WHERE condition;
```
[Note] its a Alternative to view and  vise versa   

```
select first_name, last_name
from Customer
where Country = 'London'
```
if i want this data to a new table i could use select Into function  
like this  
```
select first_name, last_name Into People_of_London
from Customer
where Country = 'London'
```
