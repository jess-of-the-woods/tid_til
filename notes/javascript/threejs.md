[notes](../notes.md) | [JavaScript](notes.md) | [3D](../3D.md) | WebGL

## Three.js



```javascript
geometry = new THREE.CubeGeometry(200, 200, 200);  // creates a new cube geometry w some parameters
material = new THREE.MeshNormalMaterial({shading: THREE.FlatShading}) // creates new material which wraps around geometry
mesh = new THREE.mesh(geometry, material); // adds new mesh which is combination of prev 2 lines ( geometry & material )
scene.add(mesh); // adds mesh to scene
```

In chrome, to allow cross origin,
close all instances then start the Chrome executable with a command line flag: `google-chrome --allow-file-access-from-files`

#### Different renderers you can use:
- WebGL
- SVG
- HTML5 Canvas

________



#### Links
- [How to effortlessly integrate Three.js into your projects]( http://bit.ly/25RlmE4) (YouTube)
- [Three.js fundamentals](https://www.pluralsight.com/courses/webgl-threejs-fundamentals) (Pluralsight course)
- [Intro to THREE.js #4 – Creating and Controlling an Animation w/ the DAT.GUI Interface](https://www.youtube.com/watch?v=GlLPYIDrxbM&list=PLOGomoq5sDLutXOHLlESKG2j9CCnCwVqg&index=4) (YouTube)
- [Gallant Lab Neuroimaging](http://gallantlab.org/semanticmovies/)
- [Interactive 3D Graphics](https://www.udacity.com/course/interactive-3d-graphics--cs291) (Udacity Course)


See Also [art](../art.md) | [canvas](../HTML/canvas.md) | [data visualisation](../dataVisualisation.md) | [SVG](../HTML/SVG.md)
