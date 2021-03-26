# SQL Overview : Types Of SQL Statements

## What is SQL

**SQL** stands for *Structured Query Language*, as it is the special purpose domain-specific language for querying data in **Relational Database Management System (RDBMS)**.

## Types of SQL Statements

SQL statements are categorized into four different types of statements

- DML (DATA MANIPULATION LANGUAGE)
- DDL (DATA DEFINITION LANGUAGE)
- DCL (DATA CONTROL LANGUAGE)
- TCL (TRANSACTION CONTROL LANGUAGE)


### DML (DATA MANIPULATION LANGUAGE)

`SELECT` Statement

The SELECT statement is used to select records from the table, with or without a condition.

- Example: Gets all records of student table.
```sql
select * from student
```
- Example: Gets records with the condition where students' rank is greater than 5.
```sql
Select * from student where rank>5
```

`INSERT`

INSERT statement is used to insert a set of values into a database table. Insert statement it used with Values.

- Example:
```sql
Insert Into Student (Rank, StudentName, Mark) Values(1,’Kumar’,450)
```

`UPDATE`

The UPDATE statement is used to update existing values in a table, which is based on some condition.

- Example: The query given below will update the studentName from Manoj to Kumar where student Name Kumar.
```sql
update student set StudentName=’Manoj’ where StudentName=’Kumar’
```

`DELETE`

Delete statement is used to delete the existing record in the table, which is based on some condition.

- Example: The query given above will delete records which has StudentName as Manoj.
```sql
Delete from Student where StudentName=’Manoj’
```

### DDL (DATA DEFINITION LANGUAGE)

`CREATE`

CREATE statement is used to create a new table in an existing database. CREATE statement is also used to create other database object such as a stored procedure, function, etc.

- Example:
```sql
Create Table Student (Rank Int, StudentName varchar(50), Mark Float)
```

`ALTER`

Alter statement can add a column, modify a column, drop a column, rename a column or rename a table.

- Example:
```sql
Alter Table Student Add (StudentAddress varchar (100))
```

`DROP`

SQL DROP TABLE statement is used to remove a table definition and all the data, indexes, triggers, constraints and permission specifications for the table.

- Example
```sql
Drop Student
```

`TRUNCATE`

TRUNCATE SQL query removes all rows from a table, without logging the individual row deletions.

- Example:
```sql
Truncate Table Table_Name
```

### DCL (DATA CONTROL LANGUAGE)

In Data Control Language(DCL), it defines the control over the data in the database. We have two different commands, which are

`GRANT`

Grant is allowed to do the specified user to the specified tasks.

Syntax

```sql
GRANT privilege_name
ON object_name
TO {user_name |PUBLIC |role_name}
[WITH GRANT OPTION];
```

`REVOKE`

It is used to cancel previously granted or denied permissions.

Syntax

```sql
REVOKE privilege_name
ON object_name
FROM {user_name |PUBLIC |role_name}
```

### TCL (TRANSACTION CONTROL LANGUAGE)

In Transaction Control Language (TCL), the commands are used to manage the transactions in the database. These are used to manage the changes made by DML statements. It also allows the statements to be grouped together into logical transactions.

`COMMIT`

Commit command is used to permanently save any transaction into the database.

Syntax

```sql
Commit;
```

`ROLLBACK`

Rollback command is used to restore the database for the last committed state. It’s also used with a save point to jump to the save point.

Syntax

```sql
Rollback to savepoint name
```

`SAVEPOINT`

SAVEPOINT command is used to temporarily save a transaction so that you can roll back to that point whenever necessary. 

Syntax

```sql
savepointsavepoint-name;
```

