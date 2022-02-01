# ASSIGNMENT

- QUERY TO FIND THE DEPARTMENT NAME THROUGH THE DEPARTMENT ID

```sql
select d.dept_name, e.dept_id, e.first_name from departments d inner join employees e on d.dept_id = e.dept_id where employee_id = 25; 
```


---

## CASCADE
```sql
alter table emp2 add FOREIGN KEY (id) references employees(id) on delete CASCADE; ` - on droping parent table the child table will also be deleted 
```

---

## WITH 
```sql
 with avg_sal as (select avg(salary) as hs from employees  - created with statement
 select * from employees, avg_sal where employees.salary > hs;  - performed with statement
```

---

## OFFSET
```sql
select * from employees limit 2 offset 3; 
```
---


# GROUPING
```sql
- group by

select name, city, state from employees group by city; 

---

- group sets

select name, city, state from employees group by grouping set ( (city), (city, state);  `
```
---


# ANY
```sql
select emp_name from employees where salary = any(select Max(salary) from employees); 
```







