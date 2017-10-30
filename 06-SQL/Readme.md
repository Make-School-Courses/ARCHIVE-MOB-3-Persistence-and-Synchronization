# SQL

In relational databases, to find data we will need to run a *query* to find our entries in tables.

Most relational databases use SQL which stands for Structured Query Language. It is a language that allows us to write code that will interact with our database.

## Objectives

- Understand why we need SQL
- Practice creating tables, entries in POSTgres
- Practice executing queries with SQL in POSTgres


## Creating a Database
## Creating Tables


## Finding entries in a table (Running Queries)

#### Get all entries in products table
```sql
select * from products
```

#### Get all entries in products table, return only name an id as a tuple

``` sql
select (name, id) from products
```

#### Get all entries in products table that have the name "Coke"

```sql
select * from products where name='Coke'
```

#### Get all entries in products table that have and id less than 2
```sql
select * from products where id<=2
```

## Creating tables

## Creating a row/entry



## Resources

[SQL Tutorials - W3School](https://www.w3schools.com/sql/)


