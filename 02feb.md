# ACCESS CONTROL LANGUAGE

- Creating user

` create user chinmay; `

- Granting access with select

` Grant select on employees to user1; `

- Providing roles to users

` alter user chinmay with CREATEDB; `

- Deleting access from a user

` revoke select on table_name from user_name; `


# TRANSACTION CONTROL LANGUAGE

- BEGIN

> untill we commit it will not update in main Database

```sql
	Begin;
	update emp2 set first_name = 'jack' where employee_id = 2;
	
```
- COMMIT 

> Now the commit will change this update in the database too.

```sql
	Begin;
	update emp2 set first_name = 'jack' where employee_id = 2;
	
	commit;
	
```

- ROLLBACK

> when we use rollback then the non-commited transaction gets rollback.

```sql
	Begin;
	update emp2 set first_name = 'jack' where employee_id = 2;
	
	Rollback;
	
```
	
	
	

