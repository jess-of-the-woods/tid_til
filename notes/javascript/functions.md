[JavaScript](index.md)

## Functions

JavaScript functions are defined with the function keyword.

### Function declaration notation
```javascript
function functionName(parameters) {
  code to be executed
}
```
e.g. (This is a named function)
```javascript
function woo() {
  console.log("Yea");
}
```

Another named function
```javascript
function triple(x) {
  return x * 3
}
```

#### Immediately Invoked Function Expression (IIFE) or 'Self-Invoking'
```javascript
;(function tripler(num){
  return num * 3
  }
})()
```
This is a function which will be Immediately invoked, because of the `()` at the end of the function.

Its important to start the line with a semi-colon '`;`' if the line would otherwise start with a parenthesis. This is important when you don't typically use semi-colons in your code.

### Function expression
```javascript
var x = function (a, b) {return a * b}
var z = x(4, 3)
```
or
```javascript
var foodDemand = function(food) {
  console.log("I want to eat" + " " + food);
}
foodDemand("Mashed Potatoes!")
// I want to eat Mashed Potatoes!
```

The functions above are actually anonymous functions (functions without names).

Functions stored in variables do not need function names. They are always invoked (called) using the variable name.

---

Functions are values. You can create an anonymous function and assign it to a variable.

e.g.
```javascript
var triple = function(x) {
  return x * 3
}
```
Just like any variable we can pass it around.. e.g.

e.g.
```javascript
var triple = function(x) {
  console.log(arguments.length);
  return x * 3
}

var waffle = triple

waffle(30)
// -> 90
```

#### Anonymous function
```javascript
function(num) {
  x = 56;
  num = num + x
  return num
}
```

### Return keyword
Parameter is a number, and we do math with that parameter
```javascript
var timesTwo = function(number) {
  return number * 2;
}
```
this calls timesTwo function and assigns output to the new variable `newNumber`, then prints newNumber to console
```javascript
var newNumber = timesTwo(8)
console.log(newNumber);
```

### Functions are Objects

JavaScript functions have both properties & methods.

The arguments.length property returns the number of arguments received when the function was invoked:

```javascript
function myFunction(a, b) {
    return arguments.length;
}
```

```javascript
type of function // function
```
---


See also hoisting in [JavaScript notes](index.md) | [objects](objects.md) | [functional programming](../functional.md)
