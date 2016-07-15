[HTML5](HTML5.md) | [notes](../notes.md)

## Canvas

### Basic Example
```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;">
</canvas>
```

### Draw a rectangle
```javascript
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.fillStyle = "#FF0000";
ctx.fillRect(0,0,150,75);
```

### Draw a circle
```javascript
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.beginPath();
ctx.arc(95,50,40,0,2*Math.PI);
ctx.stroke();
```

---

### Links
- [w3school canvas basics](http://www.w3schools.com/html/html5_canvas.asp)
- [w3school tutorial](http://www.w3schools.com/canvas/default.asp)

See also [SVG](SVG.md)
