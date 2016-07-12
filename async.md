[notes](notes.md)

## asynchronous
- [node.js](javascript/node.md)
- callbacks
- promises
- I/O - Input/Output
- filesystem read/writes, network calls
- client/server (API)
- server side rendering

---

### Breakout
```javascript
console.log('starting')

request.get('http://google.co.nz')
    .end(function(err, res)) {
        console.log('google done')
    }    

request.get('http://trademe.co.nz')
    .end(function(err, res)) {
        console.log('tm done')
    }    

console.log('all done')
```
----

Pizza order
createPizza(order, pickup)  // has anon function (pickup)

With synchronous processing, one order has to be completed before another can be taken. ('blocking')

Asynchronous doesn't work that way. I.e. is non-blocking.

Node offers easy way to do aysnchronous processing

Callbacks will always have an `error` as 1st argument, 2nd is usually `data`


See also [client-side](client-side.md) | [express.js](javascript/express.md) | [functional](functional.md) | [javascript](javascript/notes.md)
