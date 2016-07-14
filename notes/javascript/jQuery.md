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
// inserts contents of 'var' into elements with 'main' class
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

### .hide

(inside document ready function)
```javascript
$(function() {
    //hide panel 1
    $(#panel1).hide();
    //panel 2 opacity becomes 50%
}),
```
### .css

```javascript
$("#target1").css("color", "green");
$("#panel2").css({opacity:'0.5'});
```

### parent selector

```javascript
$("#target1").parent().css("background-color", "red");
```

### select even numbered elements

jQuery is zero-indexed, therefore `:even` will select 1st, 3rd, 5th elements etc.

`:odd` selects the second element, fourth element, and so on.

```javascript
$(".target:even").addClass("animated shake");
```

---
### Links
- [jQuery Tutorial for Beginners](https://www.youtube.com/playlist?list=PLoYCgNOIyGABdI2V8I_SWo22tFpgh2s6_) - LearnCode.academy - YouTube series

See also [CSS](../CSS/CSS.md) | [react](../react/react.md)
