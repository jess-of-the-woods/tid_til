[notes](../notes.md) | [frontend](../frontend.md)

## CSS - Cascading Style Sheets
**[Flexbox](flexbox.md)** | **[SASS](SASS.md)**

- [Basic Selectors](#basic-selectors)
- [The Cascade](#the-cascade)
- [Comments](#comments)
- [Pseudo-Elements](#pseudo-elements)
- [Pseudo-classes](#pseudo-classes)
- [nth-child](#nth-child)
- [Font-stack](#font-stack)
- [Layout](#layout)

### Basic Selectors

```css
body {                /* selects the body tag */
    background: red;  /* applies a red background */
}

h1 {
    font: Arial;
    color: #555;
}

```

### Classes
Classes are more specific than selecting tags. Many tags can share a class per page. Classes are represented by a `.`

```css
/* main.css */
.className {
    color: #555;
}
```
```html
<!-- index.html -->
<p class='className'>Some text</p>
<p class='className'>Yea yea yea</p>
```

### ID's
Id should exist only once per page for each id name. Typically nav. More specific than classes. Faster for browser to load. ID's are represented by a `#`

```css
/* main.css */
#special {
  font: Helvetica;
}
```
```html
<!-- index.html -->
<div id="special"></div>
```

### The Cascade
If a rule comes after a similar rule, the latter rule overrides the first rule.

More specific rules override less specific. Specificity rule

margin/padding: 4 values = top, bottom, left, right. or if just two values: top-bottom & left-right

### Comments
```css
/* comment */  
```

### Pseudo-Elements
([w3schools](http://www.w3schools.com/css/css_pseudo_elements.asp))
#### Syntax

```css
selector::pseudo-element {
    property:value;
}
```

e.g.

```css
p::first-line {
    color: #ff0000;
    font-variant: small-caps;
}
```

### Pseudo-classes
([w3schools](http://www.w3schools.com/Css/css_pseudo_classes.asp))

A pseudo-class is used to define a special state of an element.

For example, it can be used to:
- Style an element when a user mouses over it
- Style visited and unvisited links differently
- Style an element when it gets focus

#### Syntax
```css
selector:pseudo-class {
    property:value;
}
```
e.g.
```css
/* unvisited link */
a:link {
   color: #FF0000;
}

/* visited link */
a:visited {
   color: #00FF00;
}

/* mouse over link */
a:hover {
   color: #FF00FF;
}

/* selected link */
a:active {
   color: #0000FF;
}
```

### nth-child
Specify a background color for every `<p>` element that is the second child of its parent:

```css
p:nth-child(2) {
    background: red;
}
```


### Font-stack
A font stack is a list of fonts in a CSS font-family declaration. The fonts are listed in order of preference by the Web designer. A font stack allows a designer to control the look of the fonts on the Web page even if the computer doesn't have the best font for the job.

## Layout
HTML elements have default display types. e.g. divs have block type, therefore are displayed across the whole width of the page. span elements are inline, therefore are displayed inline.

### Float
clear - Specifies on which sides of an element where floating elements are not allowed to float

float -	Specifies whether or not an element should float

overflow -	Specifies what happens if content overflows an element's box

overflow-x -	Specifies what to do with the left/right edges of the content if it overflows the element's content area

overflow-y -	Specifies what to do with the top/bottom edges of the content if it overflows the element's content area

---

### Links
- [learnlayout.com](http://learnlayout.com)
- [w3schools](http://www.w3schools.com/css)

See Also [HTML](../HTML/HTML.md) | [JavaScript](../javascript/javascript.md)
