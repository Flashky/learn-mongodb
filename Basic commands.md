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
