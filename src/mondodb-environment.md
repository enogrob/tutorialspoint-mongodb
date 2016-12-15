**Start MongoDB**
```bash
brew services list
brew services start mongodb
brew services list
````

**Stop MongoDB**
```bash
brew services list
brew services stop mongodb
brew services list
````

**Restart MongoDB**
```bash
brew services list
brew services start stop
brew services start start
brew services list
````

**To use MongoDB run the following command.**

**mongo**
This will connect you to running MongoDB instance.
```
mongo
```

**MongoDB Help**
To get a list of commands, type db.help() in MongoDB client. This will give you a list of commands as shown in the following screenshot.
```
db.help() 
```

**MongoDB Statistics**
To get stats about MongoDB server, type the command db.stats() in MongoDB client. This will show the database name, number of collection and documents in the database. Output of the command is shown in the following screenshot.
```
db.stats() 
```
