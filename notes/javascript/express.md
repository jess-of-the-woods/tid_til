[backend](../backend.md) | [NPM](npm.md) | [server-side](../server-side.md)

## Express.js Server

([documentation](http://expressjs.com/))

Built on top of node core 'http' module

JSON API is quicker, more lightweight than full server-side rendering.
Read DB, send JSON to client which renders it

In express, `app.use` allows you to use middleware.. i.e. hbs, body-parser, express-sessions etc. You can also write your own middleware.

#### To setup express
* make new folder ( `mkdir newFolder` )
* `cd` into folder
* `npm init -y`
* `npm i express --save`
* `touch server.js`

#### Express Generator
`express .` to run express-generator ( run inside a folder )

or `express folderName`

---

#### Simple server example
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

#### CRUD/ REST API's
Create, Read, Update, Destroy.. See [SQL](../SQL.md)

`POST /tweets`

`GET /tweets`

`GET /tweets/:id`

`PUT /tweets/:id` ( replace whole object )

`PATCH /tweets/:id` ( replace part of object ) `{id: 7, tweet: 'hi', color: 'red'}`

`PUT /tweets/7 {color: 'blue'}` => `{id: 7, color: 'blue'}`

`PATCH /tweets/7 {color: 'blue'}` =>  `{id: 7, tweet: 'hi', color: 'blue'}`

`DELETE /tweets/:id`

#### POST Route using Knex
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

#### Passing data as query

localhost:9000/?age=33&name=will

`console.log(req.query)`

---

**if you get port in use error**, e.g. ( Error: listen EADDRINUSE :::3000 )

in terminal: `ps -ax | grep node`

You'll get something like:

60778 ??         0:00.62 /usr/local/bin/node abc.js

Then do: `kill -9 60778`

---


See also [async](../async.md) | [authentication / encryption](../auth-encryption.md)
 | [client-side](../client-side.md) |  [databases](../databases.md) | superagent
