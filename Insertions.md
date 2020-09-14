The following commands are used for inserting elements in a collection.

By default, there is no need to explicitly create a collection, when you execute an insert, the collection will be created if it doesn't already exist.

## Insert one element

Syntax:

```mongodb
db.<collection_name>.insertOne(<json>)
```

Example:

```mongodb
> db.products.insertOne({name: "A Book", price: 12.99})
{
       "acknowledged" : true,
       "insertedId" : ObjectId("5f4cd1fe17c90fd325ac7bcf")
}
```

## Insert multiple elements at once

```mongodb
db.<collection_name>.insertMany(<json>)
```

Example:

```mongodb

```
