# <b> Questions for Each Concept 
1. SQL SELECT
Write a query to retrieve all columns from the Customers table.  
Write a query to retrieve the Name and Country of all customers.   
Write a query to fetch all orders made after 2024-03-01.  
Retrieve only the Product and Price from the Orders table.  
Write a query to fetch the Email of customers who registered in 2024.  

# 2. SQL DISTINCT
Write a query to fetch distinct countries from the Customers table.  
Retrieve distinct products from the Orders table.  
Find the distinct registration dates of customers.   
Fetch distinct combinations of CustomerID and OrderDate from the Orders table.  
Write a query to retrieve all distinct prices from the Orders table.  

# 3. SQL ORDER BY
Write a query to list all customers in ascending order of their RegistrationDate.  
Retrieve all orders sorted by Price in descending order.    
Fetch the names of customers ordered alphabetically by Name.  
Retrieve the products ordered by their OrderDate in ascending order.  
List all orders sorted by Quantity in descending order and then by Price in ascending order.  

# 4. SQL WHERE
Write a query to find customers from the USA.  
Retrieve all orders where the Price is greater than 500.     
Fetch customers who registered before 2024-03-01.  
Retrieve orders where the Quantity is equal to 2.  
Write a query to fetch all products with a Price less than 300.  

# 5. SQL Comparison Operators
Fetch orders where the Price is between 200 and 800.  
Find customers whose CustomerID is greater than 2.  
Retrieve all products where the Quantity is not equal to 1.  
Write a query to fetch customers where the Country is not 'Canada'.  
Retrieve all orders where Price is equal to or greater than 800.  

# 6. SQL Logical Operators (AND, OR, NOT)
Retrieve orders where the Price is greater than 500 AND Quantity is more than 1.  
Write a query to fetch customers from the USA OR Canada.  
Retrieve orders where the Price is less than 800 AND NOT Quantity equal to 1.  
Find customers where the Country is 'USA' OR registered after 2024-02-01.  
Fetch orders where the Product is 'Laptop' AND the Price is less than 1000.  

# 7. SQL BETWEEN
Write a query to find orders with Price between 500 and 1000.  
Retrieve customers with CustomerID between 2 and 4.  
Find orders placed between 2024-03-01 and 2024-03-15.  
Fetch products with Quantity between 1 and 3.  
Retrieve customers who registered between 2024-01-01 and 2024-03-01.  

# 8. SQL IN
Write a query to find customers whose Country is in ('USA', 'Canada').  
Retrieve orders where Product is in ('Laptop', 'Smartphone').  
Fetch customers with CustomerID in (1, 3, 4).  
Retrieve orders placed on dates in ('2024-03-01', '2024-03-05').  
Fetch products where Price is in (100, 200, 800).  

# 9. SQL LIKE  
Find customers whose Email ends with '@gmail.com'.  
Retrieve customers whose Name starts with 'A'.  
Fetch products where the Product name contains 'phone'.  
Write a query to find orders where the OrderDate contains '2024-03'.  
Retrieve customers whose Name contains the letter 'i'.  

# 10. JOINS Concept
Write a query to combine Customers and Orders tables, displaying CustomerID, Name, and Product.  
Fetch all orders with their corresponding customer names.  
Retrieve customers who have placed at least one order.  
List all customers along with their OrderID, even if they haven't placed any orders.  
Display all orders, including customers from the Customers table who have no orders.  

# 11. SQL Alias (AS)
Use an alias to rename the Customers table as C and fetch Name and Country.  
Rename the Orders table as O and retrieve Product, Price, and Quantity.  
Assign an alias to the RegistrationDate column as Reg_Date and display it with Name.  
Assign an alias to the result of Price * Quantity as TotalCost and display it.  
Create an alias for the Country column as Location and display all customers' locations.  

# 12. SQL INNER JOIN
Write a query to perform an INNER JOIN between Customers and Orders on CustomerID.  
Retrieve the Name and Product for all orders.  
Display CustomerID, OrderID, and Price for all matching rows between the two tables.  
Fetch all orders made by customers in the USA.   
Retrieve the names of customers who have ordered a Laptop.   

# 13. SQL LEFT JOIN
Write a query to perform a LEFT JOIN to show all customers and their orders, if any.  
Retrieve all customers and their corresponding Product, even if they haven't ordered anything.   
Display customers who do not have any orders.  
Retrieve Name and OrderDate for all customers, even if no orders are present.  
Fetch the Name of all customers with their total order cost (if available).  

# 14. SQL RIGHT JOIN
Write a query to perform a RIGHT JOIN to show all orders and their corresponding customers, if any.  
Display all orders and their CustomerID, even if the CustomerID doesn't exist in the Customers table.  
Retrieve all OrderID and Name for matching rows between the two tables.  
Fetch CustomerID and OrderDate for all orders, even if no matching customer exists.  
Show all OrderID and their respective Country for matching records.  

# 15. SQL FULL JOIN
Write a query to perform a FULL JOIN to show all customers and their orders, including unmatched rows.  
Display all customers and orders, including rows with no matches on either side.  
Retrieve CustomerID, Name, and Product from both tables, with unmatched rows displayed as NULL.  
Find customers who do not have orders and orders that are not associated with any customer.  
Write a query to combine Customers and Orders showing Name and OrderDate, even if no matches exist.  

# 16. SQL UNION & UNION ALL
Combine the Name column from Customers with the Product column from Orders using UNION.  
Fetch all Country values from Customers and Product names from Orders, eliminating duplicates.  
Use UNION ALL to combine all CustomerID from both tables.  
Retrieve all OrderDate from Orders and RegistrationDate from Customers.  
Combine the Name column from Customers with the Product column from Orders, keeping duplicates.  

# 17. SQL Aggregate Functions
Write a query to calculate the total Price of all orders.  
Find the average Price of all orders.  
Count the total number of customers in the Customers table.  
Find the maximum Price from the Orders table.  
Retrieve the minimum RegistrationDate from the Customers table.   

# 18. SQL String Functions
Write a query to convert the Name column in Customers to uppercase.
Retrieve the first three characters of all Product names in the Orders table.
Concatenate the Name and Country columns in the Customers table.
Find the length of the Email column for all customers.
Replace '@gmail.com' with '@example.com' in the Email column.

# 19. SQL GROUP BY
Write a query to group orders by Product and count how many times each product was ordered.  
Group customers by Country and count the number of customers in each country.  
Find the total Price for each CustomerID.    
Retrieve the average Price grouped by Product.  
Display the number of orders grouped by OrderDate.  

# 20. SQL HAVING
Write a query to find products with a total Price greater than 1000 after grouping by Product.    
Retrieve customers with more than one order.  
Find all Country groups with more than two customers.  
Retrieve OrderDate groups where the average Price is greater than 500.  
Find products where the total quantity ordered exceeds 2.  

# 21. SQL Subquery: EXISTS vs IN
Use a subquery to find customers who have placed orders (use EXISTS).  
Retrieve all products ordered by customers from the USA (use IN).   
Write a query to find orders with a CustomerID in the Customers table (use IN).  
Use EXISTS to fetch customers who have placed at least one order.   
Retrieve orders where the CustomerID exists in the Customers table.  

# 22. SQL INSERT
Insert a new customer into the Customers table with the name "Eve".  
Insert a new order into the Orders table for CustomerID 3 for a "Tablet" costing 300.  
Write a query to add a new customer from "India" with the registration date "2024-04-01".  
Insert an order for CustomerID 4 for a "Monitor" with a price of 200.  
Add a new row into Orders with CustomerID 2 for a "Mouse" costing 50.  

# 23. SQL UPDATE
Update the Country of customer "Bob" to "Australia".  
Change the Price of all orders for "Laptop" to 850.   
Update the Name of the customer with CustomerID 4 to "Dina".   
Write a query to increase the Price of all products by 10%.  
Update the RegistrationDate for CustomerID 1 to "2024-02-01".  

# 24. SQL DELETE & TRUNCATE
Delete all orders where the Price is less than 100.  
Remove the customer with CustomerID 3 from the Customers table.  
Write a query to delete all rows from Orders for "Smartphone".  
Delete orders placed before "2024-03-01".  
Use TRUNCATE to remove all data from the Orders table.  

# 25. SQL CREATE Table
Write a query to create a new table named Products with columns ProductID, Name, and Category.   
Create a table Suppliers with columns SupplierID, Name, and Contact.   
Define a table Shippers with columns ShipperID, Name, and Phone.   
Write a query to create a Reviews table with columns ReviewID, CustomerID, and Rating.   
Create a Payments table with columns PaymentID, OrderID, and Amount.   

# 26. SQL ALTER Table
Add a new column Phone to the Customers table.   
Modify the Price column in Orders to accept decimal values.   
Drop the Email column from the Customers table.   
Rename the Orders table to CustomerOrders.   
Add a Status column to the Orders table with a default value of "Pending".   

# 27. SQL DROP Table
Write a query to drop the Payments table.   
Drop the Suppliers table from the database.  
Write a query to delete the Products table permanently.  
Drop the Reviews table from the schema.  
Remove the Shippers table from the database.  
