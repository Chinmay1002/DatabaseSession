# VIEWS
```sql
create view def_emp as select * from employees where employee_id between 1 and 20; `

create or replace view def_emp as select * from employees where employee_id between 1 and 20; `
```
---

# ENUM
```sql

alter table emp alter column feels TYPE varchar using feels::text; `  - ENUM TO VARCHAR

alter table emp alter column feels TYPE varchar using feels::text; ` - VARCHAR TO ENUM

alter type mood add value 'grumpy'; ` - adding value to existing enum;

```
# check
```sql
create table trial (name varchar, quantity int check(quantity<5); `
```
