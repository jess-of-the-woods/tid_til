[notes](../index.md) | [code/languages](../code.md)

## JavaScript

[asynchronous](../async.md) | [functional](../functional.md) | [ES6](es6.md)

**[jQuery](jQuery.md)** | **[Node.js](node.md)** | **[Three.js](threejs.md)**

### Table Of Contents
- [Data types](#data-types)
- [Variables](#variables)
- [Arrays](#arrays)
- [Objects](objects.md)
- [Math](math.md)
- [Functions](functions.md)
- [Comments](#comments)
- [Selectors](#selectors)
- [Events](#events)
- [Scope](#scope)
- [Hoisting](#hoisting)
- [Debugging](#debugging)
- [Conditionals](#conditionals)
- [Control Flow](control_flow.md)
- [Loops](#loops)
- [Constructors](#constructors)
- [Class](#class)
- [Closures](#closures)
- [Promises](#promises)
- [Truthy / Falsy](#truthy/falsy)
- [use strict](#use-strict)
- [Links](#links)


### Data-types
- Strings e.g. `"dogs go woof!"`
- Numbers e.g. `4`, `10`
- Booleans e.g. `false`, `5 > 4`
- Arrays e.g. `[23, bool1, {height: 154}, "stuff"]`
- Objects  e.g.

```javascript
var magrudergrind = {
  quality: 'excellent',
  genre: 'noise'
}
```

### Variables
Also referred to as a scalar. Only variables declared with keyword `var` inside functions with have 'localness'. Avoid global variables if possible.

Declare a variable and initialize (define) it to a value:
```javascript
var myAge = 34;
var myCountry = "Aotearoa"
```
The first part `var myAge` is a variable declaration, while the 2nd part `= 34` is a variable definition. These can be done separately e.g.
```javascript
var myAge // declaration of the variable 'myAge'
```
then:
```javascript
myAge = 34 // definition/initialisation of 'myAge' to '34'
```
You can also declare a bunch of variables at once like:
```javascript
var x, y, z;
```
or declare and initialize all at once:
```javascript
var variable1 = "Hello World!",
    variable2 = "Testing...",
    variable3 = 42;
```

#### typeof
tells what type a variable is (number/string/function/object etc.)
e.g.
```javascript
console.log(typeof objName);
```

#### string.replace() method
Takes string name, specifies the value within the string to be changed out, then specifies the value to be swapped in.
```javascript
var email = "jess@gmail.com"
var newEmail = email.replace("gmail","yahoo")
```
```javascript
var formattedName = HTMLheaderName.replace("%data%", bio.name);
```
#### Print substring of variable to console
x = starting position (starts from 0)
y = end position
```javascript
console.log(myCountry.substring(0,3));
```
#### Print number of characters in variable to console
```javascript
console.log(myCountry.length);
```
#### Prompt user for input and store in variable
```javascript
var age = prompt("What's your age?");
```
#### Increment/Decrement
- `variableName++` - Increment by 1
- `variableName--` - Decrement by 1
- `variableName += 3` - Increment by X (3)
- `variableName -= 3` - Decrement by X (3)

#### Convert (numerical) user input (from prompt) to a number using +
```javascript
guess = prompt()
guess = +guess;
console.log(guess);
```

### Arrays
- Lists of data
- Heterogeneous: Different data types (strings, integers, booleans)
- Ordered (position is fixed), indexed from 0
- Multidimensional (Nested, 2D, 3D etc.)
- Jagged Arrays: Nested Arrays aren't all the same length

Any time you see data surrounded by `[ ]`, it is an array.

#### Declaring/Creating an array
```javascript
var junkData = ["hello", "there", 65, 450]
```

#### Accessing data in an array
```javascript
var junkData = ["Eddie Murphy", 49, "peanuts", 31];
console.log (junkData[3])
```
prints `31`

#### Length method
```javascript
console.log(junkData.length)
```
prints out the number of items in an array

#### Push method
Arrays have a `.push()` method that adds the thing between parentheses to the end of the array. eg.

```javascript
newArray = [];
newArray.push('hello');
newArray[0];   // equals 'hello'
```
#### Iterating over an Array
```javascript
var languages = ["HTML", "CSS", "JavaScript", "Python", "Ruby"];
for (i = 0; i < languages.length; i++) {
    console.log(languages[i]);
}
```

### Comments

**Single-line**
```javascript
// Some comments
```

**Multi-line**

```javascript
/* Comment comment
comment
comment comment */
```

### Selectors
[caniuse.com](caniuse.com) - browser compatibility
```javascript
document.getElementById("main").innerHTML = "text to be <strong>entered</strong>"
document.getElementsByTagName("p")
document.getElementsByClassName("main")
document.querySelector(".main") // will give you the first element it finds
document.querySelectorAll(".main") // will give you all elements
```
```javascript
li = document.getElementsByTagName("li")
li.classList.add("main")
li.classList.remove("main")
li.parentElement.parentElement    // returns the parent of the parent
li.parentElement.children     // returns siblings
li.parentElement.children[0]   // returns sibling that is 1st child of parent
```

### Events
Event Listener is a function which takes 3 arguments:

1. Event name
2. Event Handler (which reacts to an event)
3. A Boolean

Syntax:
```javascript
source.addEventListener(eventName, eventHandler, true);
```
eg. if we have a variable `para` equal to a DOM element such as p, we can do

```javascript
para.addEventListener("mouseleave", add)
```
which will call a function called 'add'

#### Common event names
mouseout, mousemove, click, mouseover, dblclick, DomContentLoaded, load, keydown, keyup, wheel, DOMMouseScroll

#### Capturing/Bubbling
Event firing goes down the tree from the DOM element that is the root touching every child along the way, to the element which triggered it, known as the target This is capturing or phase 1. Then all the way back up again (bubbling/phase 2).
This means that with stopPropagation(), the event can be stopped at any specified point along the way.
So the 'true' boolean in the event listener means capturing. 'False' means bubbling.

### Scope
Each local scope can also see all the local scopes that contain it. JavaScript only has local & global scope. It doesn't have block scope. Functions are the only things that create local scope. All variables from blocks around a function’s definition are visible—meaning both those in function bodies that enclose it and those at the top level of the program.

#### Hoisting
When you declare and initialize a variable below other code that has the same scope, its as if the variable is being declared at the top of the code and then initialised later.
Function declarations are also hoisted, that is they are parsed before other code and therefore are available to be called before they are declared

Hoisting is JavaScript's default behavior of moving declarations to the top of the current scope.

Hoisting applies to variable declarations and to function declarations.

### Debugging
- `console.log()` to stdout
- IDE's.. visual studio, eclipse
- browser (chrome devtools) firebug for firefox
- node debugger

node inspector (lets you use devtools), can use browser to debug server side code (node-inspector &)

nodemon (file watcher)

`pgrep node`  finds process id for node

then `kill process id`

`node-inspector & nodemon --debug app.js`

typing `debugger` in code, sets breakpoint, stops code execution.
you can set breakpoints in devtools by clicking in gutter

you can hover over var's in devtools, you can change the values of var's when code exec is stopped by using console.
jump into, jump out of

### Conditionals
difference between 'else if' and 'else' is that 'else if' can take a condition, whereas else doesn't.

#### If statement
```javascript
if ("JessicaSchmessica".length < 189 ) {
  console.log("Holy crap! Your name is tiny!! Congrats my friend!" );
}
```

#### If / Else statement

```javascript
if ("This here string".length >= 99 )
{
  console.log("Let's go down the first road!");
}
else
{
  console.log("AMAZING! I guess we can travel down another road!")
}
```

### Constructors
constructs a new object with certain pre-defined properties

e.g.
```javascript
function Cat(age, color) {
  this.age = age;
  this.color = color;
}
```

### Class
In object-oriented programming, a class defines an object's characteristics. Class is a template definition of an object's properties and methods, the "blueprint" from which other more specific instances of the object are drawn.

Prototypes:
```javascript
className.prototype.newMethod = function() {
    statements;
};
```
e.g.
```javascript
function Dog (breed) {
  this.breed = breed;
};
```

Here we make buddy and teach him how to bark
```javascript
var buddy = new Dog("golden Retriever");
Dog.prototype.bark = function() {
  console.log("Woof");
};
buddy.bark();
```
here we make snoopy
```javascript
var snoopy = new Dog("Beagle");
```
This time it works!
```javascript
snoopy.bark();
```

#### Class Inheritance
```javascript
Penguin.prototype = new Animal();
```

### Closures
aka 'Lexical closures' or 'Function closures':
Being able to reference a specific instance of local variables in an enclosing function is called closure. A function that “closes over” some local variables is called a closure. This behaviour not only frees you from having to worry about lifetimes of variables but also allows for some creative use of function values.

A closure is an inner function that has access to the outer (enclosing) function’s variables—scope chain. The closure has three scope chains: it has access to its own scope (variables defined between its curly brackets), it has access to the outer function’s variables, and it has access to the global variables.

The inner function has access not only to the outer function’s variables, but also to the outer function’s parameters. Note that the inner function cannot call the outer function’s arguments object, however, even though it can call the outer function’s parameters directly.

You create a closure by adding a function inside another function.

#### Basic Example
```javascript
function showName (firstName, lastName) { 
	​var nameIntro = "Your name is ";
	    // this inner function has access to the outer function's variables, including the parameter​
	​function makeFullName () {         
	​return nameIntro + firstName + " " + lastName;     
	}
	​
	​return makeFullName (); 
	} 
	​
	showName ("Michael", "Jackson"); // Your name is Michael Jackson 
```
([Understand JavaScript Closures With Ease](http://javascriptissexy.com/understand-javascript-closures-with-ease/))

### Promises
- origami'd callback
- looks more synchronous
- 'simpler'
- Asynchronous
- promise libraries (bluebird ( denodeify ), promise ( promiseifyAll ))

### Truthy/Falsy
In JavaScript, a truthy value is a value that translates to true when evaluated in a Boolean context. All values are truthy unless they are defined as falsy (i.e., except for false, 0, "", null, undefined, and NaN).

### `'use strict'`
first introduced in ES5, but backwards compatible

reserved words, undeclared variables ( variables without using 'var' ).. will throw errors

---

### Links
- [JavaScript Glossary](https://www.codecademy.com/articles/glossary-javascript) - Codecademy

See Also [CSS](../CSS/CSS.md) | [HTML](../HTML/HTML.md)
