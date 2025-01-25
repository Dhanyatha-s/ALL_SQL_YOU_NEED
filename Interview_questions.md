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
