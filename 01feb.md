# EXPLAIN

```sql

EXPLAIN SELECT * FROM EMPLOYEES;

```

` Seq Scan on employees  (cost=0.00..22.00 rows=1200 width=40) ` - OUTPUT OF THE ABOVE QUERY


# WITH

- deleting data from one table and adding it to another table

```sql

 with rm_data as (delete from employees where salary = 8000 returning *)
 insert into emp_dup select * from rm_data;

```


# SEQUENCE
- Normal Sequence

```sql
create sequence dem start 1;
 
```
---

- Sequence with min and max value and cycle;

```sql
create sequence dem minvalue 20 maxvalue  25 start 20 cycle;

```
---

- Over 

```sql

select *, avg(salary) over (partition by dept_id) from employees;

```

---

# INDEX

- creating Index
```sql
create index emp_fname on emp2(first_name);

```

---

- Multicolumn Index

```sql
create index emp_sal_hiredate on emp2(sal, hire_date);
```
---

# CASE

```sql 
select id, first_name
case 
when salary = 18000 then 'Good'
when salary = 25000 then 'best' 
end status
from emp2;


first_name |  out  
------------+-------
 Aatmaram   | 
 Adarsh     | 
 Christie   | great
 David      | good
 Deepika    | 
 Han        | 
 Helen      | 
 Lakhan     | 
 Luna       | 
 Vandana    | 
(10 rows)

``` 
