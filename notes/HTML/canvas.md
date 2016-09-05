[HTML5](HTML5.md)

## Canvas

Canvas element is a part of HTML5 and allows for dynamic, scriptable rendering of 2D shapes and bitmap images


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
- [Canvas basics](http://www.w3schools.com/html/html5_canvas.asp) | [Tutorial](http://www.w3schools.com/canvas/default.asp) - W3School
- [HTML5 Canvas](https://www.udacity.com/course/html5-canvas--ud292) - Udacity Course
- [Canvas Tutorial](https://www.youtube.com/watch?v=FaOYjLl9dZg&list=PLftmDuo1-PWLCoCQmXM_e57bYRHjVg0pp&index=5).. (up to part 5) canvas2.html (YouTube)

See also [SVG](SVG.md)
