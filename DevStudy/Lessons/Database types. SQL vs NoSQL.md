To address most data storage problems smart math nerds created theory, that all data could be represented as a set of connected tables. Many years later we call it relational database. It uses it's own language for requests, it's called SQL(structured query language), here is an example:
``` sql
SELECT "data" FROM "User"
```
As I said, it's represented as set of tables with rows and collumns, we can play around with it in [dbdiagram](https://dbdiagram.io/d)

It suits most of modern applications, but it's very complicated at scale, so we created NoSQL databases
It stands for "Not Only SQL" by the way

Most useful for us will be Document Oriented database and MongoDB as example
``` php
db.inventory.insertOne({
	item: "journal", qty: 25, status: "A", size: { h: 14, w: 21, uom: "cm" }, tags: [ "blank", "red" ]
});
```

#SyncStudy