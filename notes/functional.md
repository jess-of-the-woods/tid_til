[notes](index.md) | [JavaScript](javascript/index.md)

## functional programming
- [Higher-order functions](#higher-order-functions)
- [Callbacks](#callbacks)
- [Closures](#closures)
- [Map](#map)
- [Filter](#filter)
- [Reduce](#reduce)
- [Uppercaser function](#uppercaser-function)
- [Recursion](#recursion)
- [Modules](#modules)
- [Links](#links)


-  All of your functions must accept at least one argument.
-  All of your functions must return data or another function.
-  No loops!


### Higher-order function
A function which takes another function as its argument (a callback)

```javascript
    function repeat(operation, num) {
      if (num <= 0) return
      operation()
      return repeat(operation, --num)
    }

    module.exports = repeat
```

### Callbacks
- Higher-order Function is another name for a Callback function
- Passing a function as an argument is called a Callback
- A callback function is a function that is passed as an argument to another function and is invoked after some kind of event.
- Functions that are passed into other functions as arguments/values are called callback functions because the host function calls back to them.

### Closures
are functions that refer to independent (free) variables. In other words, the function defined in the closure 'remembers' the environment in which it was created.

### Map
is a method on the array object. It returns all objects in the array, but transformed in a way specified by the callback function (the function which is passed to it as an argument).

#### Basic map
```javascript
function doubleAll(numbers) {
  var result = numbers.map(function(number){
    return number * 2;
  })
  return result;
}

module.exports = doubleAll
```

### Filter
Filter is a function on an array that accepts another function as its argument which it will use to return another filtered version of the array

```javascript
function getShortMessages(messages) {
  var filteredResults = messages.
    filter(function(val) {
      if (val.message.length < 50) {
        return true}
      }).
    map(function(val2) {
      return val2.message;
    });
return filteredResults;  
};

module.exports = getShortMessages
```

### Reduce
- Can do any array transformation.
- Multi-tool of list transformations. You can use it if you can't find a - pre-built transformation which suits your purposes.
- Takes 2 arguments, a starting point a.k.a accumulator (which becomes the return value in the next iteration(s) of the function), & the list ( array )

```javascript
var orders = [
  { amount: 250 },
  { amount: 400 },
  { amount: 100 },
  { amount: 325 }
]

var totalAmount = orders.reduce(function(sum, order) {
  return sum + order.amount
}, 0 )
```

### Uppercaser function
```javascript
function(input) {
  return input.toUpperCase()
}
```

### Recursion
(functional?)~~~~~~~~~~~~~~~~~

```javascript
function factorial(n) {
  if (n < 0) {
      return;
  } //termination condition

  if (n === 0) {
      return 1;
  } //base case

  return n * factorial(n - 1)  
  //recursive case
}

factorial(4);
```

### Modules
- Elm (language)
- Ramda, lodash, underscore

---

### Links
- [Functional programming in JS w/ MPJ Series](https://www.youtube.com/playlist?list=PL0zVEGEvSaeEd9hlmCXrk5yUyqUag-n84) - Just finished part 4 ( reduce advanced ) but feel like I could revise again & get more from it..  - 15 Jun
- [Higher-order functions - Part 1 of Functional Programming in JS ( MPJ )](https://www.youtube.com/watch?v=BMUiFMZr7vk&list=PL0zVEGEvSaeEd9hlmCXrk5yUyqUag-n84)
- [Callbacks & higher-order functions](http://www.niluk.co/blog/post/callbacks-and-higher-order-functions-in-javascript) - (Not Async)

See also [asynchronous](async.md) | [JavaScript functions](javascript/functions.md) | [node.js](javascript/node.md)
