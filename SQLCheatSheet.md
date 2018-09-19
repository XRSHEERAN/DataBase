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

```SQL```
```SQL```
```SQL```
```SQL```
```SQL```
```SQL```
