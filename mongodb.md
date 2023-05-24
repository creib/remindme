# MongoDB ...

## Query

### Examples
```
db.getCollection("concerts").find({'date':{$gte: ISODate('2023-05-23')}}).count()

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
