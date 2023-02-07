# SQL-STRARASCRATCH-
SQL PRACTICE

Most Profitable Companies

Find the 3 most profitable companies in the entire world.
Output the result along with the corresponding company name.
Sort the result based on profits in descending order.

forbes_global_2010_2014
| Column Name | Type    |
|-------------|---------|
|company      | varchar |
|sector       | varchar |
|industry     |varchar  |
|continent    |varchar  |
|country      |varchar  |
|marketvalue  | float   |
|sales        |float    |
|profits      |float    |
|assets       |float    |
|rank         |int      |
|forbeswebpage|varchar  |


***sql solution
```
select  top 3 profits as profit, company 
from forbes_global_2010_2014
order by profit desc;
```
