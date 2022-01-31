# Triggers


- creating function for trigger 

``` sql

create or replace function total_price()
returns trigger
As $$
declare 
total int;
begin 
total = new.price * new.copies;
return new;
end;
$$ language plpgsql;

```

---

- executing trigger to the table

``` sql

create trigger fire_total
before insert
on lib
for each row
execute procedure total_price();

```

---
