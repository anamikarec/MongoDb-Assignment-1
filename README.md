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
