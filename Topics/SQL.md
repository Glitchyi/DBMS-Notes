## Data Definition 
Used to make the definition for the database
Commands:
```SQL
- CREATE /*to create objects in the database*/
- ALTER /*alters the structure of the database*/
- DROP /*delete objects from the database*/
- COMMENT /*add comments to the data dictionary*/
- RENAME /*rename an object*/
```

#### Storage Definition
Used for internal schema definition 

#### View Definition
Used to specify external schemas

#### Data Manipulation
Used for management of data in the database like the addition updating and removal of tuples
Commands:
```SQL 
SELECT /*Retrieve data from the database*/
INSERT /*nsert data into a table*/
UPDATE /*Updates existing data within a table*/
DELETE /*deletes all records from a table*/
```

#### Data Control
```SQL 
GRANT /*Give user acces privilege */
REVOKE /*Withdraw the given privilages*/
```

#### Transaction Control
```SQL
COMMIT - save work done
ROLLBACK - restore database to original since the last commit.
```

## Data Types possible as attributes

#### NUMERIC
INTEGER/INT, SMALLINT, FLOAT/REAL, etc.

#### CHARACTER STRING
- CHAR(n)/CHARACTER(n), VARCHAR(n)/
- CHARACTER VARYING(n)/ CHAR VARYING(n), CLOB, etc.

#### BIT STRING
- BIT(n), BIT VARYING(n), BLOB etc.

#### BOOLEAN
-  3 values – true, false & unknown.

#### DATE
- 10 positions: YYYY-MM-DD

#### TIME
- 8 positions: HH:MM:SS

#### TIMESTAMP
- Includes both date and time fields.
---
## SQL COMMANDS SYNTAX
#syntax 

### CREATE
```SQL
CREATE TABLE <TABLENAME> {
	ATTRIBUTE DATATYPE,
	CONSTRAINT ()
}
```

### ALTER
```SQL
ALTER TABLE <TABLENAME> ADD/DROP/MODIFY COLUMN (DATATYPE FOR ADD AND MODIFY)
```

### DROP
Remove the entire relation
```SQL
DROP TABLE <TABLENAME> RESTRICT /* ONLY IF NO ELEMENTS*/
DROP TABLE <TABLENAME> CASCASE /*DROPS ALL OBJECTS DEPENEDED ON THE VALUE*/
 ```
 
### INSERT
New tuples
```SQL 
INSERT INTO <TABLENAME> (ATTRIBUTE NAMES) VALUES (VALUES) 
OR
INSERT INTO <TABLENAME> VALUES (VALUES)
OR
INSERT INTO <TABLENAME> VALUES (SELECT * FROM <THINGS>)
```

### DELETE
To delete tuples
```SQL 
DELETE FROM <TABLENAME> WHERE CONDITION
```

### UPDATE
update values of tuples
```SQL 
UPDATE <TABLENAME> 
SET <VALUES>
WHERE <CONDITION>
```

### SELECT 
```SQL 
SELECT <ATTRIBUTE NAMES>
FROM <TABLES>
WHERE <CONDITION>
```

### DISTINCT
Removes redundant tuples
```SQL
SELECT DISTINCT (<ATTRIBUTE NAMES>)
FROM <TABLES>
WHERE <CONDITION>
```

### LIKE 
Pattern matching situations as well as when looking for NOT NULL values
```SQL
SELECT <ATTRIBUTE NAMES> 
FROM <TABLES>
WHERE <CONDITION> LIKE <SOMETHING ELSE>
```

## Nested Queries 
A complete SELECT query, called a nested query, can be specified within the WHERE-clause of another query, called the outer query.

## Aggregate Functions 
Functions that act on a set of tuples and provide a single output
- SUM
- COUNT
- AVG
- MIN
- MAX

## GROUP BY & HAVING
The GROUP BY clause specifies the grouping attributes, which should also appear in the SELECT clause.
to apply condition to the groups that you just made we make use of the HAVING clause

## SQL Joins
#syntax 
### (INNER) JOIN:
- Select records that have matching values in both tables.
```SQL 
SELECT *
FROM <TABLE A> JOIN <TABLE B> ON <JOIN CONDITION>
WHERE <CONDITION>
```
### FULL (OUTER) JOIN:
 - Selects all records that match either left o right table records.
 ```SQL 
SELECT *
FROM <TABLE A> FULL JOIN <TABLE B> ON <JOIN CONDITION>
WHERE <CONDITION>
```
### LEFT (OUTER) JOIN:
 - Select records from the first (left-most) table with matching right table records.
```SQL 
SELECT *
FROM <TABLE A> LEFT JOIN <TABLE B> ON <JOIN CONDITION>
WHERE <CONDITION>
```
### RIGHT (OUTER) JOIN:
- Select records from the second (right-most) table with matching left table records.
```SQL 
SELECT *
FROM <TABLE A> RIGHT JOIN <TABLE B> ON <JOIN CONDITION>
WHERE <CONDITION>
```

![[Images/Pasted image 20230713172723.png]]

