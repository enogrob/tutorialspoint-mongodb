**MongoDB - Insert Document**

In this chapter, we will learn how to insert document in MongoDB collection.

**The insert() Method**

To insert data into MongoDB collection, you need to use MongoDB's `insert()` or `save()` method.

Syntax
The basic syntax of `insert()` command is as follows −
```sql
>db.COLLECTION_NAME.insert(document)
```

Example
```sql
db.mycol.insert({
   title: 'MongoDB Overview',
   description: 'MongoDB is no sql database',
   by: 'tutorials point',
   url: 'http://www.tutorialspoint.com',
   tags: ['mongodb', 'database', 'NoSQL'],
   likes: 100})
```

Here `mycol` is our collection name, as created in the previous chapter. If the collection doesn't exist in the database, then MongoDB will create this collection and then insert a document into it.

In the inserted document, if we don't specify the `_id` parameter, then MongoDB assigns a unique ObjectId for this document.

`_id` is 12 bytes hexadecimal number unique for every document in a collection. 12 bytes are divided as follows −
```sql
_id: ObjectId(4 bytes timestamp, 3 bytes machine id, 2 bytes process id,
   3 bytes incrementer)
```

To insert multiple documents in a single query, you can pass an array of documents in insert() command.

Example
```sql
db.post.insert([{
      title: 'MongoDB Overview',
      description: 'MongoDB is no sql database',
      by: 'tutorials point',
      url: 'http://www.tutorialspoint.com',
      tags: ['mongodb', 'database', 'NoSQL'],
      likes: 100
   },{
      title: 'NoSQL Database',
      description: "NoSQL database doesn't have tables",
      by: 'tutorials point',
      url: 'http://www.tutorialspoint.com',
      tags: ['mongodb', 'database', 'NoSQL'],
      likes: 20,
      comments: [{
            user:'user1',
            message: 'My first comment',
            dateCreated: new Date(2013,11,10,2,35),
            like: 0}]
}])
```

To insert the document you can use db.post.save(document) also. If you don't specify `_id` in the document then save() method will work same as insert() method. If you specify `_id` then it will replace whole data of document containing `_id` as specified in save() method.
