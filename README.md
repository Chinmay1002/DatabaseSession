# Getting started with the database(Postgres).

## Data Types
- Numeric
- Moneytary
- Character
- Binary = Bytea hex, Bytea Escape
- Date/Time Types
- Boolean 
- Enumerated = static, ordered set of values
- Geometric = point, line, lseg, box, path, path, polygon, circle.
- Network Address = cidr, inet, macaddr
- Bit String = Bit(n) and Bit(Varying)
- Text search types = tsvector, tsquery
- UUID - University unique Indentifiers
- XML = to store XML data

---

## Queries
``` 
Create Database Work;

create table badminton (pid int primary key, pname varchar, sport varchar);

insert into badminton (pname, sport) values ('leechong', 'badminton'), ('chenlong', 'badminton'), ('kevin', 'badminton'), ('gideon', 'badminton');


insert into badminton (pname, sport) values ('virat', 'cricket'), ('avesh', 'cricket'), ('sachin', 'cricket'), ('yuvraj', 'cricket');

create table cricket as select pname, sport from badminton where sport = 'cricket';

alter table cricket add constraint pr_key primary key(jerseyno);

alter table cricket add constraint fk foreign key(jerseyno) references badminton (jerseyno);

update cricket set pid=1 where pname= 'kevin';

JSON = String, Boolean, number, null
create table json(id serial not null primary key, name json);
insert into json(name) values ('{"name" : "chinmay"}');

to retrieve = select columnname -> 'targetname' as name from tablename

Arrays
create table Arrays(name text, c_id integer[], course text[][]);
insert into Arrays(name, c_id, course) values ('chinmay', '{1,2}', '{{"Maths", "Chemistry"}, {"geometry", "Science"}}');

```


