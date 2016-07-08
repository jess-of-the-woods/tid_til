[notes](../notes.md) | [to learn](../toLearn.md) | [frontend](../frontend.md)

## CSS
- [Flexbox](flexbox.md)
- [SASS](SASS.md)

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

```css
selector:pseudo-class {
    property:value;
}
```

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

## Layout
HTML elements have default display types. e.g. divs have block type, therefore are displayed across the whole width of the page. span elements are inline, therefore are displayed inline.

learnlayout(http://learnlayout.com)

See Also [HTML](../HTML/HTML.md) | [JavaScript](../javascript/javascript.md)
