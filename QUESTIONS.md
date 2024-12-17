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
