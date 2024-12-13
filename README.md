# ALL_SQL_YOU_NEED
Learn  SQL by Querying

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
> ####-- SELECT STATEMENT-- 
#### 01. Write a query to retrieve all columns from the Customers table
```--  select * from Customers```

#### 02. Name and country
``` select CustomerName, Country from Customers```

#### 03. Write a query to fetch all orders made after 2024-03-01.
```select OrderID, Product, OrderDate from Orders where Orderdate > '2024-03-01'```

#### 04. Retrieve only the Product and Price from the Orders table
```select Product, Price from Orders```

#### 05. Write a query to fetch the Email of customers who registered in 2024
```select Email from Customers where LEFT(RegistrationDate, 4) = '2024' ```
