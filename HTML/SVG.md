[HTML](HTML.md) | [notes](../notes.md) | [to learn](../toLearn.md) | [frontend](../frontend.md)

##Scalable Vector Graphics - SVG

Scalable Vector Graphics (SVG) is an XML-based markup language for describing two-dimensional vector graphics. SVG is essentially to graphics what HTML is to text.

####Setup

You can write SVG in `<svg></svg>` tags inside your HTML. Or you can write it in `<svg></svg>` tags in an svg file and link to it like so:
```HTML
<img src='fileName.svg'/>
```

####Create an SVG element on the page (A Viewport)
```HTML
<svg height="250" width="250">
</svg>
```

sets viewport size

####Specify Namespace & Version
```HTML
<svg  height='300'
      width='400'
      xmlns="http://www.w3.org/2000/svg"
      version="1.1">
</svg>
```

####Co-ordinate system
<img src='https://s3.amazonaws.com/dashingd3js/images/svg_coordinate_graph_circle_drawing_331x200.png' />

####2 Rectangles
```HTML
<rect x="0" y="0" width="150" height="150" fill="rgba(0,255,0,0.25)"></rect>
<rect x="70" y="70" width="120" height="120" fill="rgba(70,255,120,0.6)"></rect>
```

###Paths
commands are available for path data:
- M = moveto
- L = lineto
- H = horizontal lineto
- V = vertical lineto
- C = curveto
- S = smooth curveto
- Q = quadratic Bézier curve
- T = smooth quadratic Bézier curveto
- A = elliptical Arc
- Z = closepath

Note: All of the commands above can also be expressed with lower letters. Capital letters means absolutely positioned, lower cases means relatively positioned.

####Line:
`M` = 'Move to', `L` = 'Line to'

```HTML
<path d='M50 50 L200 150' stroke='black' stroke-width='20'></path>
```

####Using `<g>` tag
- group other SVG elements.
- transformations applied to `<g>` are performed on all children. attributes will be inherited
- Can group multiple elements to be referenced later with the `<use>` element.

```HTML
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
