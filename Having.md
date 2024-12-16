#### 01.Write a query to find products with a total Price greater than 1000 after grouping by Product.
```
select Product, sum(Price)as Total_price from Orders  group by Product  having sum(Price) > 1000 Order By Product
```
#### 02.Retrieve customers with more than one order.
```
select count(orderID) as Total_orders , CustomerID from Orders group by CustomerID having count(orderID) > 1 order by CustomerID
```
#### 03.Find all Country groups with more than two customers.
```
select count(CustomerID) as Total_customer, Country from Customers group by country having count(CustomerID) > 2 order by country
```
#### 04.Retrieve OrderDate groups where the average Price is greater than 500.
```
select AVG(Price) as Avg_price , OrderDate from Orders group by OrderDate having AVG(Price) > 500 order by OrderDate
```
#### 05.Find products where the total quantity ordered exceeds 2.
```
select Product, count(Quantity) as total_qnt  from Orders group by Product having count(Quantity) > 2 order by Product
```
