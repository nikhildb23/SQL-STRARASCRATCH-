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


***SQL SOLUTION
```
select  top 3 profits as profit, company 
from forbes_global_2010_2014
order by profit desc;
```

Workers With The Highest Salaries

Find the titles of workers that earn the highest salary. Output the highest-paid title or multiple titles that share the highest salary.

WORKER TABLE 
| Column Name | Type    |
|-------------|---------|
|worker_id    |int      |
|first_name   |varchar  |
|last_name    |varchar  |
|salary       |int      |
|joining_date |datetime |
|department   |varchar  |

Title Table

| Column Name    | Type    |
|----------------|---------|
|worker_ref_id   |  int    |
|worker_title    |varchar  |
|affected_from   |datetime |

***SQL SOLUTION

```
select worker_title as best_paid_title
from title left join worker on title.worker_ref_id=worker.worker_id

where salary=(select max(salary) from  worker)

```

