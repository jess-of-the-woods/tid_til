[Notes](notes.md)

#Express Server:

####To setup express:
* new folder
* cd into folder
* `npm init -y`
* `npm i express --save`
* `touch server.js`

####Express Generator:
`express .` to run express-generator ( run inside a folder )

__________________________

Use relative routes in client side app.. ( express endpoints )

__________________________

if you get port in use error, e.g. ( Error: listen EADDRINUSE :::3000 )

in terminal: `ps -ax | grep node`

You'll get something like:

60778 ??         0:00.62 /usr/local/bin/node abc.js

Then do: `kill -9 60778`

____________________

Passing data as query:

localhost:9000/?age=33&name=will

`console.log(req.query)`

___

```javascript
var express = require ('express')
var app = express()

app.get('/', function (req, res) {
    res.send ('this is a simple server')
})

app.listen(3000, function){
    console.log('Listening on port 3000!')
})
```
_________________

JSON API is quicker, more lightweight than full server-side rendering.
Read DB, send JSON to client which renders it

###CRUD/ REST APIs:
Create, Read, Update, Destroy..

`POST /tweets`

`GET /tweets`

`GET /tweets/:id`

`PUT /tweets/:id` ( replace whole object )

`PATCH /tweets/:id` ( replace part of object ) `{id: 7, tweet: 'hi', color: 'red'}`

`PUT /tweets/7 {color: 'blue'}` => `{id: 7, color: 'blue'}`

`PATCH /tweets/7 {color: 'blue'}` =>  `{id: 7, tweet: 'hi', color: 'blue'}`

`DELETE /tweets/:id`

_____________

```javascript
router.post('newTweet', function(req, res){
    knex('tweets').insert({
        tweeted: req.body.tweeted,
        userId: req.body.userId
    }).then(function(data){
        console.log(data)
    })
})
```
