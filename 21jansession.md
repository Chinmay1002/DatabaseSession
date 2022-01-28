# Joins
 ```sql
 ## Inner join
 
 
 select first_name, dept_name from employees inner join departments on employees.dept_id = departments.dept_id where salary < 15000 order by dept_name; 
 
 
 
 ## left join
 
 select employee_id, first_name from employees left join departments on employees.dept_id = departments.dept_id where salary < 10000;
 
 
 
 ## right join
 
 select employee_id, first_name, dept_name from employees right join departments on employees.dept_id = departments.dept_id where salary between 3000 and 20000 order by employee_id; 
 

 
 ## Cross join
 
 select employee_id, first_name from employees cross join departments;
 

 
 ## full join
 

 select employee_id, first_name, dept_name from employees full join departments on employees.dept_id = departments.dept_id;
 
 ```
 
 ---
 
 # ENUM
 
 ```sql
 create type mood as ENUM ('sad', 'ok', 'good');
 ```
 
 
---

# OPERATIONS

## UNION

` select * from employees UNION select * from departments; `

## INTERSECT

` select * from employees INTERSECT select * from departments; `

## UNION ALL 

` select * from employees UNION ALL select * from departments; `


## MINUS

` select * from employees MINUS select * from departments; `
