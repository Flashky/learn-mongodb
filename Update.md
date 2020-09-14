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
