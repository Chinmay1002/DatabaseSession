# Primary key

` create table employee (emp_id int PRIMARY KEY, emp_name varchar); ` - creating primary key


` alter table employee add constaint p_key PRIMARY KEY (emp_id); ` - updating a primary key



# Foreign key

` create table employee (emp_id int PRIMARY KEY, emp_name varchar, dept_id int); `

` create table departments (id serial, dept_name varchar, dept_id int references employees(dept_id) ` - creating foreign key

` alter table employees add constaint f_key Foreign key (dept_id) references employees (dept_id); `





# Not null

` create table employees (id serial, f_name varchar NOT NULL, age int); ` - creating not null constraint

` alter table employees alter column age set NOT NULL; ` - updating an existing column


# Check


` create table shop(id serial, pr_name varchar, price int check(price > 0)); `


# Unique


` create table employees1 (id serial, name varchar UNIQUE, age int); `








