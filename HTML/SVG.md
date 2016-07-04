[HTML](HTML.md) | [notes](../notes.md) | [to learn](../toLearn.md) | [frontend](../frontend.md)

##Scalable Vector Graphics - SVG

Scalable Vector Graphics (SVG) is an XML-based markup language for describing two-dimensional vector graphics. SVG is essentially to graphics what HTML is to text.

####Create an SVG element on the page:
```HTML
<svg height="250" width="250">
</svg>
```
####Specify Namespace & Version
```HTML
<svg  height='300'
      width='400'
      xmlns="http://www.w3.org/2000/svg"
      version="1.1">
</svg>
```


####2 Rectangles:
```HTML
<rect x="0" y="0" width="150" height="150" fill="rgba(0,255,0,0.25)"></rect>
<rect x="70" y="70" width="120" height="120" fill="rgba(70,255,120,0.6)"></rect>
```

###Paths
####Line:
`M` = 'Move to', `L` = 'Line to'

```HTML
<path d='M50 50 L200 150' stroke='black'stroke-width='20'></path>
```

####Using `<g>` tag
```HTML

- group other SVG elements.
- transformations applied to `<g>` are performed on all children. attributes will be inherited
- Can group multiple elements to be referenced later with the `<use>` element.

<svg viewBox="0 0 95 50"
     xmlns="http://www.w3.org/2000/svg">
   <g stroke="green" fill="white" stroke-width="5">
     <circle cx="25" cy="25" r="15"/>
     <circle cx="40" cy="25" r="15"/>
     <circle cx="55" cy="25" r="15"/>
     <circle cx="70" cy="25" r="15"/>
   </g>
</svg>
```

[MDN](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/g)


---

See also [CSS](../CSS/CSS.md) | [D3.js](../javascript/d3.md) | [react](../react/react.md)
