## INNER JOIN STATEMENTS
#### 01. Write a query to perform an INNER JOIN between Customers and Orders on CustomerID.
```
select * from Customers as c inner join Orders as o
on c.CustomerID = o.CustomerID
```
#### 02. Retrieve the Name and Product for all orders.
```
select c.CustomerName , o.Product from Orders as o
inner join  Customers as c 
on o.CustomerID = c.CustomerID
```
#### 03. Display CustomerID, OrderID, and Price for all matching rows between the two tables.
```
select c.CustomerID , o.OrderID, o.Price from Orders as o
inner join  Customers as c 
on o.CustomerID = c.CustomerID
```
#### 04. Fetch all orders made by customers in the USA.
```
select c.country,o.OrderID, o.Quantity, o.Product from Orders as o 
inner join  Customers as c 
on o.CustomerID = c.CustomerID where c.Country = 'USA'
```
#### 05. Retrieve the names of customers who have ordered a Laptop.
```
select c.CustomerName , o.Product from Orders as o 
inner join  Customers as c 
on o.CustomerID = c.CustomerID where o.Product = 'Laptop'
```
