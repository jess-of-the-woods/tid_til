#Three.js

```javascript
geometry = new THREE.CubeGeometry(200, 200, 200);  // creates a new cube geometry w some parameters
material = new THREE.MeshNormalMaterial({shading: THREE.FlatShading}) // creates new material which wraps around geometry
mesh = new THREE.mesh(geometry, material); // adds new mesh which is combination of prev 2 lines ( geometry & material )
scene.add(mesh); // adds mesh to scene
```

In chrome, to allow cross origin,
close all instances then start the Chrome executable with a command line flag: `google-chrome --allow-file-access-from-files`

####Different renderers you can use:
- WebGL
- SVG
- HTML5 Canvas

________

####Glossary:

- vertex - each angular point of a polygon, polyhedron, or other figure.
- Euler values (radians) something about pi & rotation?
- Fiducial - (especially of a point or line) assumed as a fixed basis of comparison.
- MVP - Model View Projection

####Links

[How to effortlessly integrate Three.js into your projects]( http://bit.ly/25RlmE4) ( youtube )

[Intro to THREE.js #4 – Creating and Controlling an Animation w/ the DAT.GUI Interface](bit.ly/1VpsO23)

[Gallant Lab Neuroimaging](http://gallantlab.org/semanticmovies/)

[Interactive 3D Graphics](https://www.udacity.com/course/interactive-3d-graphics--cs291)

[HTML5 Canvas](https://www.udacity.com/course/html5-canvas--ud292)

[pluralsight three.js](https://www.pluralsight.com/courses/webgl-threejs-fundamentals)
