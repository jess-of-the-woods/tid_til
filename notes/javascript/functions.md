[JavaScript](notes.md)

### Functions
This way of declaring functions is actually anonymous, although the anonymous function is stored in a variable.

```javascript
var foodDemand = function(food) {
    console.log("I want to eat" + " " + food);
}
foodDemand("Mashed Potatoes!")
// I want to eat Mashed Potatoes!
```
#### Function declaration notation:
This is a named function
```javascript
function woo() {
  console.log("Yea");
}
```

#### Another named function
```javascript
function triple(x) {
  return x * 3
}
```
#### Anonymous function
```javascript
function(num) {
  x = 56;
  num = num + x
  return num
}
```
#### Immediately Invoked Function Expression (IIFE)
```javascript
;(function tripler(num){
  return num * 3
  }
})()
```
This is a function which will be Immediately invoked, because of the `()` at the end of the function.

Its important to start the line with a semi-colon '`;`' if the line would otherwise start with a parenthesis. This is important when you don't typically use semi-colons in your code.

### Return keyword
Parameter is a number, and we do math with that parameter
```javascript
var timesTwo = function(number) {
    return number * 2;
}
```
this calls timesTwo function and assigns output to new variable (newNumber), then prints newNumber to console
```javascript
var newNumber = timesTwo(8)
console.log(newNumber);
```
