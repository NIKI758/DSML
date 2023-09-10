# Less salary

## Problem Statement:

Find the details of the employees who earn less than the average salary in their respective departments.

Note:

Return the columns 'employee_id', 'first_name', 'last_name', 'department_id', and 'salary'.
Return the output ordered by employee_id in ascending order.
Dataset Description:

![image](https://github.com/vishwasjoshi2019/DSML/assets/98074283/5d00c2e4-7459-421a-8e04-301825eafa63)


Sample Input:

Table: employees

![image](https://github.com/vishwasjoshi2019/DSML/assets/98074283/af251e02-0560-463a-9b2c-53776310d480)


Sample Output:

![image](https://github.com/vishwasjoshi2019/DSML/assets/98074283/7d9e6513-b749-4ba9-b6ff-e0ee5f2d0a89)

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
