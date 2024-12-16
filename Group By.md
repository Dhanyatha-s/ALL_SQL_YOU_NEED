#### 01. Write a query to group orders by Product and count how many times each product was ordered.
```
select Product , count(Product) as No_of_product from Orders group by Product
```
#### 02. Group customers by Country and count the number of customers in each country.
```
SELECT 
    Country, 
    COUNT(CustomerID) AS no_of_customers
FROM 
    Customers
GROUP BY 
    Country;
```
#### 03. Find the total Price for each CustomerID.
```
select Sum(Price) as Total_price , customerID from Orders group by CustomerID`
```
#### 04. Retrieve the average Price grouped by Product.
```
select Product, avg(Price) as Total_price from Orders group by Product
```
#### 05. Display the number of orders grouped by OrderDate.
```
select Count(OrderID) as Total_Orders , OrderDate from Orders group by OrderDate order by OrderDate
```
