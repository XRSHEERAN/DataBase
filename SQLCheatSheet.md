A list of SQL statements for SQLLite, tested on ipython-sql.
### Basic Table
* Create
```SQL
CREATE TABLE TBNAME(
  propertyName TYPE(INTEGER,CHAR(10), etc) PRIMARY KEY,
  ...
  //PRIMARY KEY(...,...) can be used to have key pairs
  );
```
* Select
```SQL
SELECT colname
FROM tablename
WHERE conditions (Attr='')
```
* AS
```SQL
Name AS ... //used to change the display name
```
* Math
```SQL
SELECT (Attr/100)//do math directly on  the selected row can apply
```
* Like
```SQL
... LIKE '%sample%' //contains sample
... LIKE '_ample' //anything end with ample
```
* DISTICT
```SQL
SELECT DISTINCT Attr
```
* ORDERED BY
```SQL
ODERED BY Attr DESC/ASC
```
* LIMIT
```SQL
LIMIT num
```
* Foreign Key
```SQL
FOREIGn KEY (Attr) REFERENCES TBLName(PrimaryKeyName/UniqueKeyName);
```
* CASCADE
```SQL
ON DELETE CASCADE
ON UPDATE CASCADE //pass the changes, deletes to children
ONUPDATE SET NULL //leave the foreigh key null
ON [UPDATE,DELETE] [SET NULL,CASCADE]
```
* Miltiple tables query
```SQL
SELECT A.Attr
FROM Country A, World B
WHERE A.code=B.code
AND A.Language='Test' //apply restrictions to queries
```
* Loop Query
```SQL
SELECT R.D
FROM Tbl1, Tbl2
WHERE condition
/* Equivalent to
for(i in R){
  for(j in D){}
  }
*/
```

### Advanced Features
* Set Operations
```SQL
SELECT Attr FROM tbl
INTERSECT/UNION/EXCEPT //ALL if don't remoce duplicates
SELECT Attr FROM tbl
```
Executed one tuple a time, so it is better to sort the rows first.
* Nested Queries
```SQL
SELECT C.Name
FROM (Another select) AS C
WHERE C.code=(Another select)
```
SQL is compositional, everything represents a set
* Existence
```SQL
IN (SELECT)
EXISTS(SELECT)
ANY(SELECT)
NOT EXISTS(SELECT)
ALL(SELECT)
```
* Aggregation
```SQL
SUM, AVG, COUNT, MIN, MAX
(DISTINCT AttrName)
GROUP BY AttrName
```
select element should by aggregated or the attr in group by 

```SQL

```
```SQL

```
```SQL

```
```SQL

```
```SQL

```
```SQL

```
```SQL

```
```SQL

```
```SQL

```
```SQL

```
