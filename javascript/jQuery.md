[frontend](../frontend.md) | [JavaScript](notes.md)

##jQuery

[jQuery Tutorial for Beginners](bit.ly/2383XSL)

```HTML
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.0/jquery.min.js"></script>
```

`$` sign references jQuery

In node.js projects:
```javascript
var $ = require('jquery')
```

###Syntax
```javascript
    //for id's
    $("#selector").function(propertyToBeApplied);
    // for classes
    $(".selector").function(propertyToBeApplied);

    // adds 'new' class to elements with 'main' class
    $('.main').addClass("new")

$('#main').HTML(varName)
```
Like innerHTML.. Inputs to div

####Listeners
```javascript
$(document).on('click', function() {
  //code, code, code
});
```

---

####Document ready function

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
---

####Append (or prepend) to HTML id
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

---

See also [React](../react/react.md)
