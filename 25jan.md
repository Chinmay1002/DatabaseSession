# ASSIGNMENT

` select d.dept_name, e.dept_id, e.first_name from departments d inner join employees e on d.dept_id = e.dept_id where employee_id = 25; `



---

## CASCADE

` alter table emp2 add FOREIGN KEY (id) references employees(id) on delete CASCADE; ` - on droping parent table the child table will also be deleted 




---


## WITH 

` with avg_sal as (select avg(salary) from employees ` - created with statement
` select * from employees, avg_sal where employees.salary > avg_sal; ` - performed with statement


# TRUNCATE

` create table library (id serial, book_name varchar, price int, copies int, total_price int); `



``` 
create function total_amount()
	returns trigger
	as $$
	delcare 
	total_a int;
	begin
	total_a = new.price * new.copies;
	new.total_price = total_a;
	return new;
	end;
	$$ language plpgsql;
	
```
	
---
	
``` 
create trigger total_amount
before insert 
on library
for each row
execute procedure total_amount();

```




` insert into library (book_name, price, copies) values ('TheGodfather', 300, 3), ('catch me if you can', 6000, 8), ('kevins', 3005, 12); `

--- 


## OFFSET

` select * from employees limit 2 offset 3; `

---


# GROUPING

- group by

` select name, city, state from employees group by city; `

---

- group sets

` select name, city, state from employees group by grouping set ( (city), (city, state);  `

---


# ANY
` select emp_name from employees where salary = any(select Max(salary) from employees); `







