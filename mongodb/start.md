
### MongoDB Commands
- database 
- collection
- document



starting db
> mongod

cli mongo 
> mongo

mongo help
> mongo --help

create path mongodb
> mongod --dbpath ./path-file

reset initial state
> db.dropDatabase

switch db 
> use nameDb

show all dbs
> show dbs

insert simple data 
> db.myCollection.insert({
  "valor" : 123
> })

find data in collection
> db.myColletion.find()


__

### Types data in MongoDB
- Json
- BSON (save binary in data)

` {
"name": "Wagner",
"state": "Pernambuco",
"languages": {
"javascript":7,
"sass" : 9,
}
    ` 

Pretty bson
> .find().pretty()

Data have information of data(), timestamp, second
> db.myColletion.findOne()._id.getTimestamp()

#### Search data
> db.myColletion.findOne()
> db.myColletion.findOne()._id


#### Crud
query => filter
ex: i want the document, with: b: 465
> db.myColletion.find({b:465})

if exist:
> db.myColletion.find({c: {$exists: true}})

projection
1 and 0 - true or false
> db.myColletion.findOne({}, {name: 1, rank: 1, _id: 0})
