[Notes](notes.md)

#Asynchronous
- [Node](javascript/node.md)
- callbacks
- filesystem
- client/server (API)
- restful API's
- server side rendering
- promises


###Asynchronous Breakout
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



See also Promises in js notes.
