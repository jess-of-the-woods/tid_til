[asynchronous](../async.md) | [JavaScript](notes.md) | [backend](../backend.md)

## Node.js
<a href='https://nodejs.org/en/'><img src="https://nodejs.org/static/images/logos/nodejs-new-pantone-black.png" height="120" width="200"></a>

**[NPM](npm.md)**

JavaScript had previously just run in the browser, but node takes google Chrome's V8 js engine and lets you run code on your computer.. (in command line).
- Access the files on your computer
- Listen to network traffic
- Listen to HTTP requests
- Access databases directly

Node offers easy way to do aysnchronous processing. Follows 'common.js' pattern

#### Three parts
- REPL
- Server/Package Manager ([NPM](npm.md))
- Runner ( e.g. `node fileName` to run a file with node.js runner)

'fs', 'path' & others are core node modules

### node REPL
type `node` in terminal (with no arguments) to enter REPL
- `.save fileName.js`: saves the session as a file
- `.load fileName.js`: loads a session from a file
- `.help`: displays available commands
- 'ctrl + c' to exit

### Commands
- `node fileName`: to run a file with Node runner
- `node -v` or `node --version`: To see if Node is installed, tells you version number
- `npm -v`: To see if NPM is installed, tells you version number
- `node --help`: Help
- `which node` finds path of node install

### fs (file system) module
part of 'core node'
```javascript
var fs = require('fs')
var output = fs.readFileSync('data.txt', 'utf8')
```
utf8 is character encoding.. converts from buffer i.e. (b4 7v 3g....) to readable data

### http module
```javascript
var http = require('http')
var server = http.createServer(function(req, res){

})
server.listen(3000)

```


### Modules & Exports / Requires

```javascript
//module1
var m2 = require('./module2')
m2()

```
```javascript
// module2
module.exports = function(){
  console.log('I\'m module 2!');
}
// or
function a(){
  console.log('I\'m module 2!');
}
module.exports = a


```
or
```javascript

//module1
console.log(m2);
console.log(typeof m2);

```

```javascript
// module2
var a = 1
module.exports.a = a
module.exports.b = 2

//or

exports.a = a // this will export {a: 1}, type: object

// or

module.exports = a // this will export 1 (type: number)

```

To execute a function exported inside an object: `objectName.functionName()`

---

### Links
- [An introduction to Node.js - Max Ogden](https://github.com/maxogden/art-of-node)
- [process.argv](http://code-maven.com/argv-raw-command-line-arguments-in-nodejs) (part of node.js tutorial, http://code-maven.com )
- [Understanding module.exports and exports in Node.js](https://www.sitepoint.com/understanding-module-exports-exports-node-js/)
- [Learn Node.js with Brigadier Fluffykins Part I: Sync, Async, and Creating Your First Server!](https://medium.freecodecamp.com/learn-node-js-with-brigadier-fluffykins-i-basics-async-sync-create-your-first-server-b9e54a45e108#.x7dcs09wk)

See also [bundling](../bundling.md) | [functional programming](../functional.md) | [networks](../networks/index.md)
