[frontend](../frontend.md) | [client-side](../client-side.md) | [JavaScript](notes.md)

## jQuery
<a href="https://jquery.com/"><img src="http://ejohn.org/apps/workshop/adv-talk/jquery_logo.png" width='300'></a>

jQuery is a cross-platform JavaScript library designed to simplify the client-side scripting of HTML

Link to jQuery library in html:
```HTML
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.0/jquery.min.js"></script>
```

`$` sign references jQuery

In node.js projects:
```javascript
var $ = require('jquery')
```

### Syntax
```javascript
//for id's
$("#selector").function("propertyToBeApplied");
// for classes
$(".selector").function("propertyToBeApplied");
```
e.g.
```javascript
// adds 'new' class to elements with 'main' class
$('.main').addClass("new")

$('#main').html(varName)
```

`.html` is like innerHTML (in vanilla js).. Inputs to div

### Listeners
```javascript
$(document).on('click', function() {
  //code, code, code
});
```

### Document Ready function

Everything should go inside this 'Document.ready' function. Waits till page is loaded then fires.
```javascript
    $(document).ready(function() {
            // code, code, code
        });
```
or alternatively
```javascript
    $(function() {
      // code, code, code
    });
```

### Append (or prepend) to HTML id
(Udacity Resume Assignment)

```javascript
$("#header").append(variableName);
```

---

```javascript
$(function() {
    //hide panel 1
    $(#panel1).hide();
    //panel 2 opacity becomes 50%
    $(#panel2).css({opacity:'0.5'});
}),
```
### .css

```javascript
$("#target1").css("color", "green");
```

### parent selector
```javascript
$("#target1").parent().css("background-color", "red");
```

---
### Links
- [jQuery Tutorial for Beginners](https://www.youtube.com/playlist?list=PLoYCgNOIyGABdI2V8I_SWo22tFpgh2s6_) - LearnCode.academy - YouTube series

See also [react](../react/react.md)
