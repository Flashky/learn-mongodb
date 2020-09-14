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

Syntax:

```mongodb
db.<collection_name>.insertMany(<json_array>)
```

Example:

```mongodb
db.flightData.insertMany([
  {
    "departureAirport": "MUC",
    "arrivalAirport": "SFO",
    "aircraft": "Airbus A380",
    "distance": 12000,
    "intercontinental": true
  },
  {
    "departureAirport": "LHR",
    "arrivalAirport": "TXL",
    "aircraft": "Airbus A320",
    "distance": 950,
    "intercontinental": false
  }
])
```

Also, we will get an acknowledge, with as may ids as inserted objects:

```mongodb
{
        "acknowledged" : true,
        "insertedIds" : [
                ObjectId("5f5f22ca599c49b894bd494f"),
                ObjectId("5f5f22ca599c49b894bd4950")
        ]
}
```
