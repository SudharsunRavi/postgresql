### PostgreSQL

SQL engine for used to query DB
Open source relational DB
Easy for handling large volumes of stuctured data
Offers ACID properties (Atomicity, Consistency, Isolation, Durability) and supports transactions which ensure data integrity

### pgAdmin

Free and open source adminsitration and development platform for managing postgreSQL databases
Provides GUI interface, also gives range of features for databse management

## SELECT
```select columnName from tableName (* - for all values)```

# select unique values only
```select distinct columnName from tableName``` 

# count no.of rows, giving * includes null values
```select count(*) from tableName```

# count no.of rows, giving columnName ignores NULL val.
```select count(columnName) from tableName```

# count no.of rows excluding duplicates
```select count(distinct columnName) from tableName```

# select with conditions
```select * from tableName where columnName > 1000  ```

# select with conditions multiple conditions
```select * from tableName where columnName > 1000 AND/OR .... ```

## operators involved in conditions

=
<> or !=
>
>=
<
<=
between
like --> %, _
in
is NULL
NOT, AND, OR

like 'A%' --> starts with A
like '%A' --> ends with A
like '%A%' --> has A

# order by- sort the result set of a query in specified sequence
# by default ascending
```select * from tableName where ... order by columnName1 ASC, columnName2 DESC ... ```
# here the column1 will first take everything in ascending and will go for column2 and make it descending with respect to column1

Example:

Rank    Student_Name
1       Austin
1       Hello
1       Hi
2       Hey
1       Whatsupp?
3       Wassupp
4       Supp
2       Nooo
2       Nothing
5       Noicee
2       Boring
3       PSQL

Output:

Rank    Student_Name

1       Whatsupp
1       Hi
1       Hello
1       Austin
2       Nothing
2       Nooo
2       Hey
2       Boring
3       Wassupp
3       PSQL
4       Supp
5       Noicee

# limit command-used to restrict no.of rows returned by query
# advantages: 
    performance optimization
    pagination
    rsource management

```select * from tableNmae limit 10```

## Aggregate Functions
    1. Grouping
    2. Common aggregate- sum(), count(), avg(), max(), min(), round()
        -provide columnName inside paranthesis

```select min(columnName), max(columnName), avg(columnName) from tableName```

-using round off
```select round(avg(columnName), 3) from tableName```
    -here it restricts to 3decimal values

# group by- used to group rows from a table on one or more columns.

# having- used to filter rows in the result set after grouping, aggregation
#       - follows GROUP BY clause
















