
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

drop terminal with --logpath or --syslog
> mongod --dbpath ./path-file --fork 
> mongod --dbpath ./path-file --fork --logpath /var/log/mongodb/

**Filter process in my terminal**
ps aux | grep mongo


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

Where are logs 
> cat mongo.log

first ten lines
> tail mongo.log -f
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


Create
> insert( {} )
> insertOne( {} )
> insertMany([ {}, {} ])

other infos:
Continue insert with error 
> ordered : true //default
Ex
> db.dados.inserMany([{a:12},{b:25},{c:456}])
___

Read
> find()
> findOne
___

Update
> Update
> updateOne
> updateMany
___

Detele
> deleteOne
> deleteMany
