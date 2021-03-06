[JavaScript](index.md)

### ES6 / ECMAScript 2015

ES6 is a significant update to the JavaScript language, and the first update to the language since ES5 was standardised in 2009

### New features
- generator function
- yield keyword
- destructuring
- arrow functions
- var, let, const

### let
A new way to declare & define variables i.e.
```javascript
let i = 10 // instead of var i = 10
```
Introduces block scope. let is scoped to blocks, such as for loops, if statements etc.. i.e. anything between two curly braces.

### const
A new type of variable which can not be reassigned.

```javascript
const x = {coffee: 'yum'}
console.log(x); //
```
You can
Common use cases include port numbers in node apps, API keys for 3rd party API's, things like `const pi = 3.14 ` etc.

### Arrow Functions

```javascript
// es5 code
var createGreeting = function (message, name) {
  return message + name;
}
```

```javascript
// equivalent done with ES6 arrow function
var arrowGreeting = (message, name) => {
  return message + name
};
```
You don't have to include the return keyword when you don't have braces. Also if there is only one argument to the function, you need need parentheses surrounding the args.

```javascript
var arrowGreeting = name => name;
```

```javascript
var squared = x => x * x;
```

### Babel
Babel transforms ES6 code into readable and standards-compliant ES5 code that can be executed by JavaScript engines that haven't implemented ES6.

Babel can transpile ES6 code on the server, or it can run directly on the client. You can also install Babel globally so you can use it in the terminal.

ES6 allows you to write your web application logic such that it runs on both the server and the client, the definition of Isomorphic JavaScript. You can also use the more recent term Universal JavaScript to describe the same code running in different environments.

### Arrow functions
Arguments first, followed by an arrow `=>` followed by the function body.


### Links
- [ES6 with Babel](http://code.tutsplus.com/courses/start-coding-es6-with-babel/lessons/babel-on-the-client) (up to part 2)
