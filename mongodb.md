# MongoDB ...

## Query

### Examples
```
db.getCollection("concerts").find({'date':{$gte: ISODate('2023-05-23')}}).count()

```

## Backup and restore
### Create the dump
```
mongodump --host=db.hostname.de --port=27047 --username=mongo_admin --password=xxx --authenticationDatabase=admin --forceTableScan --gzip --db=testdb --out=mongo-db-$(date +"%Y_%m_%d_%I_%M_%p")
```

### Restore the dump
```
mongorestore --host=db2.hostname.de --port=27048 --username=mongo_admin --password=xxx --authenticationDatabase=admin --gzip ./mongo-db-2023_05_21_04_34_PM
```

## Operations

### Get and kill running operations
```
# get the operations
db.currentOp()

# kill with operation id
db.killOp(8499123.0)
```

## Users

### Get User
```
use testdb
db.getUsers()
```
### Create User
```
use testdb
db.createUser(
   {
     user: "testdbusername",
     pwd: "xxx",
     roles:
       [
         { role: "readWrite", db: "testdb" }
       ]
   }
)
```
### Drop User
```
use testdb
db.dropUser("testdbusername")
```
