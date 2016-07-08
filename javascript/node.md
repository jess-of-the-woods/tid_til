[notes](../notes.md) | [JavaScript](notes.md) | [asynchronous](../async.md) | [backend](../backend.md)

## Node.js
<a href='https://nodejs.org/en/'><img src="https://nodejs.org/static/images/logos/nodejs-new-pantone-black.png" height="120" width="200"></a>

**[NPM](npm.md)** | **[express.js](express.md)**

Node offers easy way to do aysnchronous processing. Follows common.js pattern

#### Three parts
- REPL
- Server ([NPM](npm.md))
- Runner

fs & path are core node modules

### Commands
`node fileName`: to run a file with Node runner

`node -v`: To see if Node is installed, tells you version number

`npm -v`: To see if NPM is installed, tells you version number

`node --help`: Help

`which node` finds path of node install

`npm -g ls`: prints list of all globally installed modules

`npm -g ls --depth=0`

`npm uninstall moduleName --save`: uninstalls module & deletes reference in package.json


### fs ( file system )
```javascript
var fs = require('fs')
var output = fs.readFileSync('data.txt', 'utf8')
```
utf8 is character encoding.. converts from buffer i.e. (b4 7v 3g....) to readable data

### Bundling
making require work in browser

Once you have node.js or io.js, open terminal. Run `npm init` to create a package.json, then `npm i browserify --save-dev`.

Then inside package.json, insert a script in script tags..
`build: 'browserify app.js -o bundle.js'`

This will then be able to be run from terminal by 'npm run build', assuming you called the script build.

Then you can add a script tag (link) to bundle.js in your html file.

Live Reload / Budo / Watchify / Nodemon / Webpack


### Links
- [An introduction to Node.js - Max Ogden](https://github.com/maxogden/art-of-node)
- [process.argv](http://code-maven.com/argv-raw-command-line-arguments-in-nodejs) (part of node.js tutorial, http://code-maven.com )
- [Understanding module.exports and exports in Node.js](https://www.sitepoint.com/understanding-module-exports-exports-node-js/)
- [Getting started with Browserify](https://www.youtube.com/watch?v=CTAa8IcQh1U) (YouTube)

---

See also bundling | [functional programming](functional.md)
