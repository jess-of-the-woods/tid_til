[notes](../notes.md) | [asynchronous](../async.md) | [JavaScript](notes.md) | [backend](../backend.md)

## Node.js
<a href='https://nodejs.org/en/'><img src="https://nodejs.org/static/images/logos/nodejs-new-pantone-black.png" height="120" width="200"></a>

**[NPM](npm.md)**

Node offers easy way to do aysnchronous processing. Follows 'common.js' pattern

#### Three parts
- REPL ( type `node` in terminal to enter REPL )
- Server/Package Manager ([NPM](npm.md))
- Runner ( e.g. `node fileName` to run a file with node.js runner)

'fs' & 'path' are core node modules

### Commands
`node fileName`: to run a file with Node runner

`node -v` or `node --version`: To see if Node is installed, tells you version number

`npm -v`: To see if NPM is installed, tells you version number

`node --help`: Help

`which node` finds path of node install


### fs ( file system module )
```javascript
var fs = require('fs')
var output = fs.readFileSync('data.txt', 'utf8')
```
utf8 is character encoding.. converts from buffer i.e. (b4 7v 3g....) to readable data

---

### Links
- [An introduction to Node.js - Max Ogden](https://github.com/maxogden/art-of-node)
- [process.argv](http://code-maven.com/argv-raw-command-line-arguments-in-nodejs) (part of node.js tutorial, http://code-maven.com )
- [Understanding module.exports and exports in Node.js](https://www.sitepoint.com/understanding-module-exports-exports-node-js/)
- [Learn Node.js with Brigadier Fluffykins Part I: Sync, Async, and Creating Your First Server!](https://medium.freecodecamp.com/learn-node-js-with-brigadier-fluffykins-i-basics-async-sync-create-your-first-server-b9e54a45e108#.x7dcs09wk)

See also [bundling](../bundling.md) | [functional programming](../functional.md)
