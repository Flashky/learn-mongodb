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

## Update an existing element

Update command needs two arguments:

- One for filtering which element to update.
- Another one for updating the element itself.

The syntax is a bit more complicated, as you need to use a $set to specify the new or new fields:

```mongodb
db.<collection_name>.updateOne(<json_filter>, {$set: <json_new_fields>)
```

The following update will find a flight having a distance to 12000 and then add a marker field to it:

```mongodb
db.flightData.updateOne({distance: 12000}, {$set: {marker: "delete"}})
```

## Update all elements

updating all elements is as simple as using updateMany and keeping the filter with empty curly braces:

```mongodb
db.flightData.updateMany({}, {$set: {marker: "delete"}})
```

## Replace an existing element

Pending

## Deleting an existing element

```mongodb
db.products.deleteOne({name: "A Book"})
```

The previous sentence will delete the first document which has a name attribute valued as "A Book".

In the case we want to delete using the id:

```mongodb
db.products.deleteOne({ _id: ObjectId("5f4cd1fe17c90fd325ac7bcf") })
```

## Clear screen

To clear your screen just type ``cls``:

```mongodb
> cls
```
