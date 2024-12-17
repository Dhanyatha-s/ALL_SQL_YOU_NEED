### Creating new Table Product

```
SELECT * FROM questions.products;
```
#### Create Table "Products"
```
create table Products ( 
ProductID int primary Key auto_increment, 
Product varchar(255),
Price int,
ManufacturingDate date
)
```
#### Add the Column OrderID 
```
Alter table questions.products add column OrderID Int
```

#### Make that OrderID Column to be Foreign Key Constraint
```
Alter table questions.products add constraint OrderID foreign key (OrderID) references questions.Orders (OrderID)
```
#### Insert values Into It.
```
insert into questions.products(Product,Price,ManufacturingDate, OrderID) values ('Laptop', 4000, '2024-01-01', 2),
('Smartphone' ,700, '2024-06-01',5),
('Tablet', 450,	'2024-06-05', 1)
```
## Practice Questions

#### 01.Replace NULL values in Price with 0 using COALESCE.
```
select OrderID, coalesce(Price, 0) as ModifiedPrice from questions.products
```


