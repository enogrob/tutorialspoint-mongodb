**MongoDB - Create Database**

In this chapter, we will see how to create a database in MongoDB.

**The use Command**
MongoDB use DATABASE_NAME is used to create database. The command will create a new database if it doesn't exist, otherwise it will return the existing database.

**Syntax**
Basic syntax of use DATABASE statement is as follows −

```
use DATABASE_NAME
```

**Example**
If you want to create a database with name <mydb>, then use DATABASE statement would be as follows −
```
use mydb
switched to db mydb
```

To check your currently selected database, use the command db
```
db

mydb
```

If you want to check your databases list, use the command show dbs.
```
show dbs

local     0.78125GB
test      0.23012GB
```
Your created database (mydb) is not present in list. To display database, you need to insert at least one document into it.
```javascript
db.movie.insert({"name":"tutorials point"})

show dbs

local      0.78125GB
mydb       0.23012GB
test       0.23012GB
```
`
In MongoDB default database is test. If you didn't create any database, then collections will be stored in test database.
