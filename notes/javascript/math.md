[JavaScript](index.md) | [maths](../math/index.md)

## javascript math

### random numbers

`Math.random()` returns a random number between 0 & 1
e.g.
```javascript
var x = Math.random()
```

### floor

Returns the largest integer less than or equal to a number.

syntax:

```javascript
Math.floor(expression)
```
example:

```javascript
Math.floor(9.99); // 9
Math.floor(1 + 0.5); // 1
Math.floor(Math.random() * X + 1); // Returns a random number between 1 and X
```
Return a whole number between 0 & 10:
```javascript
Math.floor(Math.random() * 11)

```

how does this work?
`Math.floor(Math.random() * 5 + 1);`
First we use Math.random() to create a random number from 0 up to 1. For example, 0.5
Then we multiply by 5 to make the random number from 0 up to 5. For example, 0.5 * 5 = 2.5    
Next we use Math.floor() to round down to a whole number. For example, Math.floor( 2.5 ) = 2
Finally we add 1 to change the range from between 0 and 4 to between 1 and 5 (up to and including 5)

### pow

Returns base raised to exponent.

Syntax:
```javascript
Math.pow(base,exponent)
```
Example

```javascript
Math.pow(2,4); // gives 16
```
[Read more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/pows)

### ceil

Returns the smallest integer greater than or equal to a number.

Syntax

```javascript
Math.ceil(expression)
```
Example

```javascript
Math.ceil(45.4); //  46
Math.ceil(4 - 1.9); //  3
```
[Read more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/ceil)

### PI

Returns the ratio of the circumference of a circle to its diameter, approximately 3.14159 or in better terms, the value of PI (π). Note in syntax , we do not put () at the end of Math.PI because Math.PI is not a function.

Syntax:
```javascript
Math.PI
```

Example

```javascript
Math.round(Math.PI); // rounds the value of PI ,gives 3
Math.ceil(Math.PI); // 4
```
[Read more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/PI)

### sqrt

Returns the square root of a number.

Syntax:

```javascript
Math.sqrt(expression)
```
Example

```javascript
Math.sqrt(5+4); // 3
Math.sqrt(Math.sqrt(122+22) + Math.sqrt(16)); //4
```
[Read more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/sqrt)

### numbers
#### % (modulus/modulo)

It returns the remainder left after dividing the left hand side with the right hand side.

syntax:

```javascript
number1 % number2
```
example:

```javascript
14 % 9 // returns 5
```

`23%10` = 23 divided by 10 = 2 and a remainder of 3

#### isNaN

Returns true if the given number is not a number, else returns false.

syntax:

```javascript
isNaN([value])
```
example:

```javascript
var user_input = prompt("Enter a number"); // Enter "a number"

if(isNaN(user_input))
    alert("I told you to enter a number.");

//alert executed , since "a number" is not a number

//Another important thing:

if( isNaN("3") )
    alert("bad");

//Not executed , because the string "3" gets converted into 3 ,and 3 is a number
```
### basic arithmetic

Doing basic arithmetic is simple.

syntax:

```javascript
4 + 5;  // 9
4 * 5;  // 20
5 - 4;  // 1
20 / 5; // 4
```
#### prefix & postfix increment/decrement operators

Prefix increment / decrement operators are operators that first increase the value of the variable by 1 (increment) or decrease the value of an expression / variable by 1 (decrement) and then return this incremented / decremented value. They are used like ++(variable) [increment] or --(varaible) [decrement] On the other hand , Postfix increment / decrement operators are operators that first return the value of the variable and then increase the value of that variable by 1 (increment) or decrease the value of the variable by 1 (decrement) . They are used like (variable)++ [increment] or (varaible)-- [decrement]

syntax:

```javascript
--variable   //Prefix Decrement
++variable   //Prefix Increment
variable--   //Postfix Decrement
variable++  //Postfix Increment
```
example:
```javascript
//The examples will make it clear

var x = 15; // x has a value of 15
var y = x++;
// since it is postfix , the value of x (15) is first assigned to y and then the value of x is incremented by 1
console.log(y); //15
console.log(x); //16

var a = 15; // a has a value of 15
var b = ++a;
// since it is prefix , the value of a (15) is first incremented by 1 and then the value of x is assigned to b
console.log(b); //16
console.log(a); //16
```
