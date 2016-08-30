[JavaScript](index.md)

## Control Flow

### Logical operators
`&&` - and

`||` - or

`!` - not

```javascript
var programming = false;

var happy = function() {
  if (!programming) {
       return true;
  }
  else {
      return false;
  }
};
```

### Switches
```javascript
var someVariable = prompt("type something")

switch (/*Some expression*/) {
    case 'option1':
        // Do something
        break;
    case 'option2':
        // Do something else
        break;
    case 'option3':
        // Do a third thing
        break;
    default:
       // Do yet another thing
}
```

### Loops

#### For loops
You use for loops, if you know how often you'll loop. The most often used varName in loops is i.

Syntax:
for(initialisation, condition, mutator) {
  do something()
};

e.g.
```javascript
for (var counter = 1; counter < 6; counter++) {
  console.log(counter);
}
```
or

```javascript
for (var i = 1; i < 11; i = i + 1){
  console.log(i);
}
```

#### For / In Loop
loop over objects.
```javascript
var nyc = {
    fullName: "New York City",
    mayor: "Bill de Blasio",
    population: 8000000,
    boroughs: 5
};

for(var vertebrae in nyc) {
    console.log(vertebrae);
}
```
will print property names, even though there is no 'vertebrae' property in nyc object.

#### While loops
Used when you don't know how many times a loop will have to execute.. While 'some condition' is true, run code, then check condition again.

```javascript
while(condition) {
//Do something
}
```
e.g.

```javascript
var goop = 0;
while (goop < 52) {
goop++
    console.log(goop);
}
```
or

```javascript
var count = 0
var loop = function() {
	while(count < 3) {count++
		console.log("I'm looping!")
	}
}
loop();
```
or

```javascript
var counter = true;
var soloLoop = function(){
  while(counter){
      console.log("Looped once!");
      counter = false;
  }
};
soloLoop();
```

#### Do/While Loop (a.k.a "Do" loops)
Runs at least one time no matter what. Checks the condition after running once. And if still true will loop again.

```javascript
var loopCondition = false;

do {
	console.log("I'm gonna stop looping 'cause my condition is " + loopCondition + "!");
} while (loopCondition);
```
or
```javascript
var getToDaChoppa = function (number) {
  var val = number - 1;
  do {
      console.log("Ah yes! Quite!");
  }
  while(getToDaChoppa < 1);
};
getToDaChoppa(1);
```
or

```javascript
var huh = true;
do {
   console.log("huh huh?");
   huh = false;
}
while (huh);
```
