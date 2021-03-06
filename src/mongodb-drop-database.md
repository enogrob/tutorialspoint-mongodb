**MongoDB - Drop Database**

In this chapter, we will see how to drop a database using MongoDB command.

**The dropDatabase() Method**
MongoDB db.dropDatabase() command is used to drop a existing database.

Syntax
Basic syntax of dropDatabase() command is as follows −

*db.dropDatabase()*
This will delete the selected database. If you have not selected any database, then it will delete default 'test' database.

Example
First, check the list of available databases by using the command, show dbs.
```
>show dbs
local      0.78125GB
mydb       0.23012GB
test       0.23012GB
>
```
If you want to delete new database <mydb>, then dropDatabase() command would be as follows −
```
>use mydb
switched to db mydb
>db.dropDatabase()
>{ "dropped" : "mydb", "ok" : 1 }
>
```
Now check list of databases.
```
>show dbs
local      0.78125GB
test       0.23012GB
>
```
