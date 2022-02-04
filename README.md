#### For this assignment you need to create a database called assignment and collection called users that has following fields :-
- first_name
- last_name
- email
- gender
- ip_address
- age

> Step:- 1 For the database, show all the databases already present:~
- Input
```js
    show dbs
```
- Output
```js
    admin       0.000GB
    config      0.000GB
    local       0.000GB
    test        0.000GB
```
> Step:- 2 Create and use a db named assignment
- Input
```js
    use assignment
```
> Then use 
- Input
```js
    show dbs
```
- Output
```js
    admin       0.000GB
    assignment  0.000GB
    config      0.000GB
    local       0.000GB
    test        0.000GB
```
> inside the db <assignment> show collection
- Input
```js
    show collections
```
- Output
```js
    // will be empty initially
```
> create collection named users
- Input
```js
    db.createCollection('users')
```
- Output
```js
    // output will be empty initially, since no data is available
```
##### Insert 10 documents in this users collection using both insert and insertMany
~ For the insertion of single document-
```js
db.users.insertOne({
        "_id" : ObjectId("61fcc8406239fe038cf25ba7"),
        "id" : 11,
        "first_name" : "kaina",
        "last_name" : "frdggf",
        "email" : "rde0@hugedomains.com",
        "gender" : "Female",
        "ip_address" : "182.212.228.243",
        "age" : 31
}
```
~ For the insertion of multiple documents
```js
db.users.insertMany([{
        "_id" : ObjectId("61fcc8406239fe038cf25ba9"),
        "id" : 1,
        "first_name" : "Ruthy",
        "last_name" : "Gilbride",
        "email" : "rgilbride0@hugedomains.com",
        "gender" : "Female",
        "ip_address" : "182.212.228.243",
        "age" : 36
}
{
        "_id" : ObjectId("61fcc8406239fe038cf25baa"),
        "id" : 2,
        "first_name" : "Charlot",
        "last_name" : "de Grey",
        "email" : "cdegrey1@google.ru",
        "gender" : "Female",
        "ip_address" : "29.226.157.201",
        "age" : 74
}
{
        "_id" : ObjectId("61fcc8406239fe038cf25bab"),
        "id" : 3,
        "first_name" : "Leigh",
        "last_name" : "McEachern",
        "email" : "lmceachern2@usda.gov",
        "gender" : "Female",
        "ip_address" : "32.27.27.197",
        "age" : 14
}
{
        "_id" : ObjectId("61fcc8406239fe038cf25bac"),
        "id" : 4,
        "first_name" : "Sandy",
        "last_name" : "Tissell",
        "email" : "stissell3@cdbaby.com",
        "gender" : "Bigender",
        "ip_address" : "49.233.211.155",
        "age" : 20
}
{
        "_id" : ObjectId("61fcc8406239fe038cf25bad"),
        "id" : 5,
        "first_name" : "Karissa",
        "last_name" : "Poynter",
        "email" : "kpoynter4@flavors.me",
        "gender" : "Male",
        "ip_address" : "180.60.48.186",
        "age" : 4
}
{
        "_id" : ObjectId("61fcc8406239fe038cf25bae"),
        "id" : 6,
        "first_name" : "Grace",
        "last_name" : "Strevens",
        "email" : "gstrevens5@mediafire.com",
        "gender" : "Male",
        "ip_address" : "82.132.71.222",
        "age" : 41
}
{
        "_id" : ObjectId("61fcc8406239fe038cf25baf"),
        "id" : 7,
        "first_name" : "Anamika",
        "last_name" : "Bowker",
        "email" : "bbowker6@typepad.com",
        "gender" : "Male",
        "ip_address" : "142.30.74.204",
        "age" : 30
}
{
        "_id" : ObjectId("61fcc8406239fe038cf25bb0"),
        "id" : 8,
        "first_name" : "Lev",
        "last_name" : "Cavaney",
        "email" : "lcavaney7@odnoklassniki.ru",
        "gender" : "Male",
        "ip_address" : "70.139.209.229",
        "age" : 24
}
{
        "_id" : ObjectId("61fcc8406239fe038cf25bb1"),
        "id" : 9,
        "first_name" : "Inessa",
        "last_name" : "Magarrell",
        "email" : "imagarrell8@yellowpages.com",
        "gender" : "Female",
        "ip_address" : "253.88.8.137",
        "age" : 58
}
{
        "_id" : ObjectId("61fcc8406239fe038cf25bb2"),
        "id" : 10,
        "first_name" : "Wileen",
        "last_name" : "Tezure",
        "email" : "wtezure9@123-reg.co.uk",
        "gender" : "Female",
        "ip_address" : "211.52.142.226",
        "age" : 97
}
{
        "_id" : ObjectId("61fcc8d36239fe038cf25bb3"),
        "first_name" : "Maggie",
        "last_name" : "Breens",
        "email" : "mbreens1@weibo.com",
        "gender" : "Female",
        "ip_address" : "201.15.26.74",
        "age" : 35
}])
```
##### Select all the documents in the users collection using find and also a single document using findOne
- To find the elements in the collection
```js
    db.users.find()
```
- To find the single element in the collection
```js
    db.users.findOne({"first_name":"Anamika"})
```
##### Update at least 3 documents using update and updateMany
~ for single one
```js
     db.users.update({"first_name" : "Anamika"},{$set : {"first_name":"Princess"}})
```
~ for multiple updation
```js
     db.users.updateMany({"gender" : "Female"},{$set : {"gender":"Male"}})
```
##### Delete documents using remove, remove that will remove just 1 document, deleteOne, deleteMany
- deleteOne
```js
    db.users.remove({"first_name": "Anamika"})
```
- deleteMany
```js
    db.users.deleteMany({"gender": "Male"})
```
##### Delete db named assignment
```js
    db.dropDatabase()
```
