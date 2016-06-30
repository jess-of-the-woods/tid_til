[JavaScript](notes.md) | [Frontend](../frontend.md)

##jQuery

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.0/jquery.min.js"></script>
```

[jQuery Tutorial for Beginners](bit.ly/2383XSL)


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

___________

Everything should go inside this 'Document.ready' function. Waits till page is loaded then fires.
```javascript
    $(document).ready(function() {
            // code, code, code
        });
```
or
```javascript
    $(function() {
      // code, code, code
    });
```
---

###Listeners
```javascript
    $(document).on('click', function() {
        //code, code, code
    });
```

---

####Udacity Resume Assignment

append (or prepend) to html id
```javascript
$("#header").append(variableName);
```

---

```javascript
$(function() {
    $(#panel1).hide();
    $(#panel2).css({opacity:'0.5'});

}),
```
//hide panel 1
//panel 2 opacity becomes 50%

See also [React](../react/react.md) |
