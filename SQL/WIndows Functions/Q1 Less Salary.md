# Less salary

## Problem Statement:

Find the details of the employees who earn less than the average salary in their respective departments.

Note:

Return the columns 'employee_id', 'first_name', 'last_name', 'department_id', and 'salary'.
Return the output ordered by employee_id in ascending order.
Dataset Description:

![261920361-5d00c2e4-7459-421a-8e04-301825eafa63](https://github.com/NIKI758/DSML/assets/63571840/fcb89e47-db90-49a9-9e23-eb4786e2c119)


Sample Input:

Table: employees

![261920375-af251e02-0560-463a-9b2c-53776310d480](https://github.com/NIKI758/DSML/assets/63571840/c2af4208-25a1-4bdd-b138-9087814f1d89)



Sample Output:


![261920392-7d9e6513-b749-4ba9-b6ff-e0ee5f2d0a89](https://github.com/NIKI758/DSML/assets/63571840/4433489f-501c-48be-beac-57d0221444ae)

---

## Solution

```sql
select employee_id,first_name,last_name,department_id,salary
from
(select *,avg(salary) over(partition by department_id) as avg_sal
from employees) t
where salary<t.avg_sal
 order by employee_id
```
