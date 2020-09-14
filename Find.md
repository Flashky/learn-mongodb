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
```

Result:

```mongodb
{
       "_id" : ObjectId("5f4cd1fe17c90fd325ac7bcf"),
       "name" : "A Book",
       "price" : 12.99
}
```

## Find with filters


Syntax:

```mongodb
db.<collection_name>.find(<json>)
```

Example:

```mongodb
 db.flightData.find({intercontinental: false}).pretty()
```

The result will filter any elements from the collection having the intercontinental attribute set to false:

```mongodb
{
        "_id" : ObjectId("5f5f22ca599c49b894bd4950"),
        "departureAirport" : "LHR",
        "arrivalAirport" : "TXL",
        "aircraft" : "Airbus A320",
        "distance" : 950,
        "intercontinental" : false
}
```

