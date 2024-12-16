# ALL_SQL_YOU_NEED
Learn  SQL by Querying

> # Get All the Query Questions here  [Clcik on Link](https://github.com/Dhanyatha-s/ALL_SQL_YOU_NEED/blob/main/QUERIES.md)


## Here is the SQL SCRIPT

>### Step 1: Create Database SQLTUTORIAL
### Step 2: Create tables and Insert values to them.
```
-- Create Customers Table
CREATE TABLE Customers (
    CustomerID INT PRIMARY KEY AUTO_INCREMENT,  -- Auto-incrementing unique identifier
    Name VARCHAR(100) NOT NULL,                 -- Customer name
    Email VARCHAR(100) UNIQUE NOT NULL,         -- Customer email
    Country VARCHAR(50) NOT NULL,               -- Customer country
    RegistrationDate DATE NOT NULL              -- Registration date
);

-- Insert Sample Data into Customers Table
INSERT INTO Customers (Name, Email, Country, RegistrationDate) VALUES
('Alice', 'alice@gmail.com', 'USA', '2024-01-15'),
('Bob', 'bob@gmail.com', 'Canada', '2024-02-10'),
('Charlie', 'charlie@gmail.com', 'UK', '2024-03-05'),
('Diana', 'diana@gmail.com', 'USA', '2024-03-15');

-- Create Orders Table
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY AUTO_INCREMENT,     -- Auto-incrementing unique identifier
    CustomerID INT NOT NULL,                    -- Foreign key to Customers table
    Product VARCHAR(100) NOT NULL,              -- Name of the product
    Quantity INT NOT NULL,                      -- Quantity ordered
    Price DECIMAL(10, 2) NOT NULL,              -- Price of the product
    OrderDate DATE NOT NULL,                    -- Order date
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID) -- Define foreign key relationship
);

-- Insert Sample Data into Orders Table
INSERT INTO Orders (CustomerID, Product, Quantity, Price, OrderDate) VALUES
(1, 'Laptop', 1, 800.00, '2024-03-01'),
(2, 'Smartphone', 2, 1000.00, '2024-03-02'),
(3, 'Headphones', 1, 200.00, '2024-03-05'),
(1, 'Keyboard', 2, 100.00, '2024-03-10'),
(4, 'Laptop', 1, 800.00, '2024-03-20');
```
## -- SELECT STATEMENT--

#### 01. Write a query to retrieve all columns from the Customers table
```
--  select * from Customers
```

#### 02. Name and country
```
select CustomerName, Country from Customers
```

#### 03. Write a query to fetch all orders made after 2024-03-01.
```
select OrderID, Product, OrderDate from Orders where Orderdate > '2024-03-01'
```

#### 04. Retrieve only the Product and Price from the Orders table
```
select Product, Price from Orders
```

#### 05. Write a query to fetch the Email of customers who registered in 2024
```
select Email from Customers where LEFT(RegistrationDate, 4) = '2024'
```

## -- ORDER BY STATEMENT--


#### 01. Write a query to list all customers in ascending order of their RegistrationDate.
```
SELECT CustomerName, RegistrationDate
FROM Customers Order By RegistrationDate ASC
```

#### 02. Retrieve all orders sorted by Price in descending order.
```
 select * from Orders order by Price DESC
```

#### 03. Fetch the names of customers ordered alphabetically by Name.
```
select CustomerName from Customers order by CustomerName
```

#### 04. Retrieve the products ordered by their OrderDate in ascending order.
```
select Product, OrderDate from Orders order by OrderDate ASC
```

#### 05. List all orders sorted by Quantity in descending order and then by Price in ascending order.
```
select * from Orders order by Quantity DESC, Price
```

## -- WHERE  STATEMENT --

#### 01. Write a query to find customers from the USA.
```
select CustomerName from Customers where Country = 'USA'
```

#### 02.Retrieve all orders where the Price is greater than 500.
```
select * from Orders where Price > 500
```

#### 03. Fetch customers who registered before 2024-03-01.
```
select CustomerName, RegistrationDate from Customers where RegistrationDate < '2024-03-01'
```

#### 04.Retrieve orders where the Quantity is equal to 2.
```
select * from Orders where Quantity = 2
```

#### 05. Write a query to fetch all products with a Price less than 300
```
select * from Orders where Price < 300
```


## -- COMPARISION OPERATORS --

#### 01. Fetch orders where the Price is between 200 and 800.
```
select * from Orders where Price between 200 and 800
```

#### 02. Find customers whose CustomerID is greater than 2.
```
select CustomerName, CustomerID from Customers where CustomerID > 2
```

#### 03. Retrieve all products where the Quantity is not equal to 1.
```
select Product, Quantity from Orders where Quantity <> 1
```

#### 04. Write a query to fetch customers where the Country is not 'Canada'.
```
select CustomerName from Customers where Country <> 'Canada'
```

#### 05. Retrieve all orders where Price is equal to or greater than 800.
```
select * from Orders where Price >= 800
```

## -- LOGICAL OPERATORS --

#### 01. Retrieve orders where the Price is greater than 500 AND Quantity is more than 1.
```
SELECT * FROM Orders where Price > 500 and Quantity > 1
```

#### 02. Write a query to fetch customers from the USA OR Canada.
```
select CustomerName, Country from Customers where Country = 'USA' or Country = 'Canada'
```

#### 03. Retrieve orders where the Price is less than 800 AND NOT Quantity equal to 1.
```
 select * from Orders where Price < 800 and Quantity <> 1
```

#### 03. Find customers where the Country is 'USA' OR registered after 2024-02-01. 
```
select CustomerName, Country from Customers where Country = 'USA' or RegistrationDate = '2024-02-01'
```

#### 04. Fetch orders where the Product is 'Laptop' AND the Price is less than 1000
```
 select * from Orders where Price < 1000 and Product = 'Laptop'
```
## --  BETWEEN --

#### 01. Write a query to find orders with Price between 500 and 1000.
```
 select * from Orders where Price between 500 and 1000
```
#### 02. Retrieve customers with CustomerID between 2 and 4.
```
select CustomerName, CustomerID from Customers where CustomerID between 2 and 4
```
#### 03. Find orders placed between 2024-03-01 and 2024-03-15.
```
 select * from Orders where OrderDate between '2024-03-01' and '2024-03-15'
```

#### 04. Fetch products with Quantity between 1 and 3.
```
 select Product, Quantity from Orders where Quantity between 1 and 3
```
#### 05. Retrieve customers who registered between 2024-01-01 and 2024-03-01.
```
 select CustomerName, RegistrationDate from Customers where RegistrationDate between '2024-01-01' and '2024-03-01'
```
## -- IN --

#### 01. Write a query to find customers whose Country is in ('USA', 'Canada').
```
 select CustomerName, Country from Customers where Country in ('USA', 'Canada')
```

#### 02. Retrieve orders where Product is in ('Laptop', 'Smartphone').
```
select * from Orders where Product in ('Laptop', 'Smartphone')
```

#### 03. Fetch customers with CustomerID in (1, 3, 4).
```
 select CustomerName, CustomerID from Customers where CustomerID in (1,3,4)
```

#### 04. Retrieve orders placed on dates in ('2024-03-01', '2024-03-05').
```
 select * from Orders where OrderDate in ('2024-03-01', '2024-03-05')
```

#### 04. Fetch products where Price is in (100, 200, 800).
```
 select Product from Orders where Price in (100, 200, 800)
```

## -- LIKE --

#### 01. Find customers whose Email ends with '@gmail.com'.
```
select CustomerName, Email from Customers where Email like '%@gmail.com'
```

#### 02. Retrieve customers whose Name starts with 'A'.
```
select CustomerName from Customers where CustomerName like 'A%'
```

#### 03. Fetch products where the Product name contains 'phone'.
```
select Product from Orders where Product like '%Phone%'
```

#### 04. Write a query to find orders where the OrderDate contains '2024-03'.
```
select OrderDate from Orders where OrderDate like '%2024-03_%'
```

#### 05. Retrieve customers whose Name contains the letter 'i'.
```
 select CustomerName from Customers where CustomerName like '%i%'
```
## -- JOINS Concept --
#### 01. Write a query to combine Customers and Orders tables, displaying CustomerID, Name, and Product.
```
select Customers.CustomerID, Customers.CustomerName, Orders.Product from Customers 
Inner Join  Orders on Customers.CustomerID = Orders.CustomerID
```

#### 02. Fetch all orders with their corresponding customer names.
```
select o.OrderID, o.Product, o.Quantity, o.Price, c.CustomerName from Orders as o 
Inner Join  Customers as c  on o.CustomerID = c.CustomerID
```

#### 03. Retrieve customers who have placed at least one order.
```
select o.OrderID, o.Quantity,  C.CustomerName from Customers as C join Orders as o on C.CustomerID = o.CustomerID where o.Quantity = 1
```

#### 04. List all customers along with their OrderID, even if they haven't placed any orders.
```
select c.customerID, c.CustomerName, o.OrderID from Customers as c join Orders as o on c.CustomerID = o.CustomerID
```

#### 05. Display all orders, including customers from the Customers table who have no orders.
```
select c.CustomerID, c.CustomerName, o.OrderID, o.Product, o.Quantity, o.Price from Customers as c Left join Orders as o on c.CustomerID = o.OrderID
```

# IF YOU HAVE CAME HERE KUDOOS💪😁💪 NOW GO TO THE FILE FOR INTERMEDIATE PRACTICES
