## Find all elements from a collection

Syntax:

```mongodb
db.<collection_name>.find()
```

Example:

```mongodb
> db.products.find()
{ "_id" : ObjectId("5f4cd1fe17c90fd325ac7bcf"), "name" : "A Book", "price" : 12.99 }
```

## Pretty printing results

Just add ``print()`` to any sentence to a find command to make it pretty printed:

```mongodb
> db.products.find().pretty()
{
       "_id" : ObjectId("5f4cd1fe17c90fd325ac7bcf"),
       "name" : "A Book",
       "price" : 12.99
}
```
