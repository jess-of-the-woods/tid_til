[notes](notes.md)

## Bundling / Building

Making require work in browser

### Browserify
Once you have node.js or io.js, open terminal. Run `npm init` to create a package.json, then `npm i browserify --save-dev`.

Then inside package.json, insert a script in scripts section:
```json
"build": "browserify app.js -o bundle.js"
```

You can then run from terminal with `npm run build`

Then you can add a `<script src="bundle.js">` tag in your html file.

Example scripts:
```json
"build": "browserify . -o bundle.js -g uglifyify"
"test": "browserify test.js | node | tap-spec"
```
see also **watchify / hbsfy**

### budo
a browserify server for rapid prototyping ([npm page](https://www.npmjs.com/package/budo))
```json
"start": "budo . -d --serve bundle.js --live"
```

### gulp
- [Babel-starters-kit](https://github.com/jess-of-the-woods/Babel-starters-kit)

### webpack

install globally with `npm i webpack -g`

run with `webpack`

webpack.config.js

options include watch (for file changes) `webpack --watch`

#### webpack-dev-server
There is also 'webpack-dev-server', hot-reloads changes. Doesn't build file. Needs to be installed globally as a separate module.

checkout localhost:8080/webpack-dev-server

---

See also [deployment](deployment.md) | [npm](javascript/npm.md)

- npm scripts
- Task runners...? (Grunt, Gulp),
- Live Reload?
- uglifyify
- minify

### Links
- [Getting started with Browserify](https://www.youtube.com/watch?v=CTAa8IcQh1U) - YouTube
- [Beginner’s guide to Webpack](https://medium.com/@dabit3/beginner-s-guide-to-webpack-b1f1a3638460#.anh3ggrrl)
- Asynchronous Module Definition [Why AMD](http://requirejs.org/docs/whyamd.html) |  [Wiki](https://en.wikipedia.org/wiki/Asynchronous_module_definition)
