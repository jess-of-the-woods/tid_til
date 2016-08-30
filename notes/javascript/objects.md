[JavaScript](index.md)

### Objects
A JavaScript object is a collection of named values
Like a noun & a verb together. Information & Functions in the same place.
You can also think of objects as combinations of key-value pairs (like arrays), only their keys don't have to be numbers like 0, 1, or 2: they can be strings and variables
- have properties, and properties have values
- have methods (like a function associated with an object)

#### Object Literal Notation
```javascript
var myObj = {
    type: 'fancy',
    disposition: 'sunny'
};

var emptyObj = {};
```

#### Object Constructor
```javascript
var objectName = new Object();
```
#### Accessing Objects

##### Dot notation
`bob.name`

e.g.
```javascript
var newVar = bob.name;
```

##### Bracket Notation
`bob["name"];`

e.g.
```javascript
var newVar = bob["name"];
```

##### 2 ways to add keys/values to object
```javascript
myObj["name"] = "Charlie";
```
or
```javascript
myObj.name = "Charlie";
```
#### Object Methods
here is bob again, with his usual properties
```javascript
var bob = new Object();
bob.name = "Bob Smith";
bob.age = 30;
```
this time we have added a method, setAge
```javascript
bob.setAge = function (newAge){
  bob.age = newAge;
};
bob.setAge(20);
```
'this' is a place holder used in methods (functions), (defined outside of an object). Replace 'this' with the object name and the method can be used on any object.

##### hasOwnProperty (Object Method)
checks to see whether an object has a particular property

e.g.
```javascript
var suitcase = {
    shirt: "Hawaiian"
};

if (suitcase.hasOwnProperty('shorts')) {
    console.log(suitcase.shorts);
}
else {
    suitcase.shorts = "red";
}
```

---

See also [functions](functions.md)
