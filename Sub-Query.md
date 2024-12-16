#### 01. Use a subquery to find customers who have placed orders (use EXISTS).
```
SELECT  CustomerName, CustomerID from Customers c1 where exists (select OrderID from Orders o1 where c1.CustomerID = o1.CustomerID)
```
#### 02. Retrieve all products ordered by customers from the USA (use IN).
```
select Product from Orders where CustomerID IN (select CustomerID from Customers where Country = 'USA')
```
#### 03. Write a query to find orders with a CustomerID in the Customers table (use IN).
```
select CustomerName from Customers c1 where CustomerID in (select CustomerID from Orders o1 where c1.CustomerID = o1.CustomerID)
```
#### 04. Use EXISTS to fetch customers who have placed at least one order.
```
SELECT CustomerName
FROM Customers c1
WHERE EXISTS (
    SELECT 1
    FROM Orders o
    WHERE c1.CustomerID = o.CustomerID
);
```
#### 05. Retrieve orders where the CustomerID exists in the Customers table.
```
SELECT CustomerID
FROM orders o
WHERE EXISTS (
    SELECT CustomerID
    FROM customers c
    WHERE o.CustomerID = c.CustomerID
);
```
