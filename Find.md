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

## Find one element

Syntax:

```mongodb
db.<collection_name>.findOne()
```

Example:

```mongodb
db.flightData.findOne()
```

Find one will find just the first result, even if there are multiple elements:

```mongodb
{
        "_id" : ObjectId("5f5f22ca599c49b894bd494f"),
        "departureAirport" : "MUC",
        "arrivalAirport" : "SFO",
        "aircraft" : "Airbus A380",
        "distance" : 12000,
        "intercontinental" : true
}
```

## Filtering results

You can filter both your ``find()`` and ``findOne()`` results by just adding a json as a parameter:

Syntax:

```mongodb
db.<collection_name>.find(<json_filter>)
db.<collection_name>.findOne(<json_filter>)
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

### Greater than / Lesser than filers

In case you want any values starting from or ending at some point, then you need to use ``$gt`` or ``$lt`` keyword within curly braces.

Syntax:

```mongodb
db.<collection_name>.find({<attribute>: {$gt: <value>})
```

Example:

```mongodb
> db.flightData.find({distance: {$gt: 950}}).pretty()
```

Result will be any flights having a distance greater than 950:

```mongodb
{
        "_id" : ObjectId("5f5f22ca599c49b894bd494f"),
        "departureAirport" : "MUC",
        "arrivalAirport" : "SFO",
        "aircraft" : "Airbus A380",
        "distance" : 12000,
        "intercontinental" : true
}
```
