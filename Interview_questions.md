## Write a query to summarize the total sales revenue for each product line. 
## The product line with the highest revenue should be at the top of the results.

```
select distinct p.product_line,
sum(amount)  over (partition by p.product_line) as total_revenue
from transactions t
inner join 
product_info as p
on t.product_id = p.product_id
order by total_revenue desc
```
## As an employee at NVIDIA, you've been given access to the customer records database. The Sensors team is interested in understanding which customers are interested in Artificial Intelligence (AI). The relevant fields are:
```
create table customer_interest (customer_id int primary key,
c_name varchar(50),
email varchar(50),
interest varchar(50))

insert into customer_interest (customer_id, c_name, email, interest) values 
(1234, "john" ,"johnsmith@email.com", "Gaming, AI, Data Center"),
(5678,	"Mary Johnson"	,"maryj@email.com",	"Gaming, Autonomous Machines"),
(9123,	"James Williams"	,"jamesw@email.com"	, "AI,Autonomous Machines"),
(4567,	"Patricia Brown"	,"patriciab@email.com"	,"Data Center, AI")

```
```
select customer_id, c_name, interest from customer_interest
where interest like "%AI%"
```
