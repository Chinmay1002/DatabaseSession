# Database with clauses

``` sql
create table employees(id serial primary key, name varchar,gender varchar, salary int, designation varchar);


create table employees(id serial primary key, name varchar,gender varchar, salary int, designation varchar); 


insert into employees(name, gender, salary, designation) values ('chinmay', 'M', 1300, 'dev'), ('suyash', 'M', 2000, 'dev'), ('sachin', 'M', 2500, 'devops'), ('mitali', 'F', 3000, 'dev'), ('nikita', 'F', 5000, 'frontend'), ('jayshree', 'F', 4500, 'data science'), ('bhumika', 'F', 3600, 'dev'), ('deepak', 'M', 4100, 'data analyst'), ('anurag', 'M', 2500, 'data science'), ('sumit', 'F', 4600, 'devops'), ('geet', 'M', 6100, 'frontend'); 

```

---
``` sql
 select * from employees;
 id |   name   | gender | salary | designation  
----+----------+--------+--------+--------------
  1 | chinmay  | M      |   1300 | dev
  2 | suyash   | M      |   2000 | dev
  3 | sachin   | M      |   2500 | devops
  4 | mitali   | F      |   3000 | dev
  5 | nikita   | F      |   5000 | frontend
  6 | jayshree | F      |   4500 | data science
  7 | bhumika  | F      |   3600 | dev
  8 | deepak   | M      |   4100 | data analyst
  9 | anurag   | M      |   2500 | data science
 10 | sumit    | F      |   4600 | devops
 11 | geet     | M      |   6100 | frontend 
 
 ```
 
 ---


  


``` sql

select count(*), gender, designation from employees group by designation, gender;

 count | gender | designation  
-------+--------+--------------
     1 | F      | data science
     1 | M      | frontend
     1 | M      | devops
     1 | M      | data analyst
     2 | M      | dev
     1 | F      | devops
     1 | F      | frontend
     1 | M      | data science
     2 | F      | dev
     
```


---


``` sql

select designation, gender, count(*) from employees where salary between 2000 and 5000 group by gender, designation;

 designation  | gender | count 
--------------+--------+-------
 data science | F      |     1
 dev          | F      |     2
 devops       | F      |     1
 frontend     | F      |     1
 data analyst | M      |     1
 data science | M      |     1
 dev          | M      |     1
 devops       | M      |     1
 
```


---

 

``` sql
select designation, gender, count(*) from employees where salary < 4000 group by gender, designation;
 designation  | gender | count 
--------------+--------+-------
 dev          | M      |     2
 dev          | F      |     2
 devops       | M      |     1
 data science | M      |     1
 
 ```



---





```sql

select id from employees order by id desc limit 1;

 id 
----
 11 
 
 ---


```
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

