## SQL LEFT JOIN

#### 01. Write a query to perform a LEFT JOIN to show all customers and their orders, if any.
```
select c.CustomerID, c.CustomerName,  o.OrderID, o.Product, o.Quantity, o.Price 
from Customers as c 
Left join Orders as o on c.CustomerID = o.CustomerID
```
#### 02. Retrieve all customers and their corresponding Product, even if they haven't ordered anything.
```
select  c.CustomerName, o.Product 
from Customers as c 
Left join Orders as o on c.CustomerID = o.CustomerID
```
#### 03. Display customers who do not have any orders.
```
select c.CustomerID, c.CustomerName
from Customers as c 
Left join Orders as o on c.CustomerID = o.CustomerID  where o.OrderID is null
```
#### 04. Retrieve Name and OrderDate for all customers, even if no orders are present.
```
select c.CustomerName, o.OrderDate
from Customers as c 
Left join Orders as o on c.CustomerID = o.CustomerID 
```
#### 05. Fetch the Name of all customers with their total order cost (if available).
```
select c.CustomerName, 
coalesce(sum(o.Price), 0) as Total_cost
from Customers as c
Left join Orders as o 
on c.CustomerID = o.CustomerID
Group By c.CustomerID, c.CustomerName
```

