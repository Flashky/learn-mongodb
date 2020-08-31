## Show databases

```mongodb
> show dbs
admin   0.000GB
config  0.000GB
local   0.000GB
```

## Change database

```mongodb
> use local
switched to db local
```

## Create a new database

Just use the same ``use`` command:

```mongodb
> use shop
switched to db shop
```

## Create a new collection

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



## Clear screen

To clear your screen just type ``cls``:

```mongodb
> cls
```
