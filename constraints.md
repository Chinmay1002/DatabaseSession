# Primary key

` create table employee (emp_id int PRIMARY KEY, emp_name varchar); ` > creating primary key


` alter table employee add constaint p_key PRIMARY KEY (emp_id); ` > updating a primary key



# Foreign key

` create table employee (emp_id int PRIMARY KEY, emp_name varchar, dept_id int); `

` create table departments (id serial, dept_name varchar, dept_id int references employees(dept_id) ` > creating foreign key




# Not null
