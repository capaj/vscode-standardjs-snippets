# vscode-standardjs-snippets
same snippets as https://github.com/gaboesquivel/atom-standardjs-snippets but for Visual Studio Code

## Standard JavaScript Snippets for Visual studio code

A collection of ES6 snippets for faster JavaScript development in [Atom Editor](https://atom.io/).  

This collection is complementary to [atom/language-javascript](https://github.com/atom/language-javascript). It's based on [extrabacon/atom-turbo-javascript](https://github.com/extrabacon/atom-turbo-javascript) and it enforces [standardjs code style](http://standardjs.com/).

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

__Yes!, no semicolons:__
- [Are Semicolons Necessary in JavaScript?](https://www.youtube.com/watch?v=gsfbh17Ax9I)
- [An Open Letter to JavaScript Leaders Regarding Semicolons](http://blog.izs.me/post/2353458699/an-open-letter-to-javascript-leaders-regarding)
- [JavaScript Semicolon Insertion - Everything You Need to Know](http://inimino.org/~inimino/blog/javascript_semicolons)


## Snippets

Snippets are optimized to be short and easy to remember.

- [declarations](#declarations)
- [flow control](#flow-control)
- [functions](#functions)
- [iterables](#iterables)
- [objects and classes](#objects-and-classes)
- [returning values](#returning-values)
- [types](#types)
- [promises](#promises)
- [ES6 modules](#es6-modules)
- [testing](#testing)
- [console](#console)
- [timers](#timers)
- [DOM](#dom)
- [Node.js](#nodejs)
- [miscellaneous](#miscellaneous)

### Declarations

#### `v⇥` var statement
```js
var ${1:name}
```

#### `va⇥` var assignment
```js
var ${1:name} = ${2:value}
```

#### `l⇥` let statement
```js
let ${1:name}
```

#### `la⇥` let assignment
```js
let ${1:name} = ${2:value}
```

#### `ly⇥` let yielded assignment
```js
let ${1:name} = yield ${2:value}
```

#### `c⇥` const statement
```js
const ${1:name}
```
#### `cd⇥` const from destructuring
```js
const {${1:name}} = ${2:value}
```

#### `ca⇥` const assignment
```js
const ${1:name} = ${2:value}
```

#### `cy⇥` const yielded assignment
```js
const ${1:name} = yield ${2:value}
```

### Flow Control

#### `i⇥` if statement
```js
if (${1:condition}) {
  ${0}
}
```

#### `el⇥` else statement
```js
else {
  ${0}
}
```

#### `ife⇥` else statement
```js
if (${1:condition}) {
  ${0}
} else {

}
```

#### `ei⇥` else if statement
```js
else if (${1:condition}) {
  ${0}
}
```

#### `fl⇥` for loop (ES6)
```js
for (let ${1:i} = 0, ${2:len} = ${3:iterable}.length ${1:i} < ${2:len}; ${1:i}++) {
  ${0}
}
```

#### `fi⇥` for in loop (ES6)
```js
for (let ${1:key} in ${2:source}) {
  if (${2:source}.hasOwnProperty(${1:key})) {
    ${0}
  }
}
```

#### `fo⇥` for of loop (ES6)
```js
for (let ${1:key} of ${2:source}) {
  ${0}
}
```

#### `wl⇥` while loop
```js
while (${1:condition}) {
  ${0}
}
```

#### `tc⇥` try/catch
```js
try {
 ${0}
} catch (${1:err}) {

}
```

#### `tf⇥` try/finally
```js
try {
 ${0}
} finally {

}
```

#### `tcf⇥` try/catch/finally
```js
try {
  ${0}
} catch (${1:err}) {

} finally {

}
```

### Functions

#### `f⇥` anonymous function
```js
function (${1:arguments}) {${0}}
```

#### `fn⇥` named function
```js
function ${1:name}(${2:arguments}) {
  ${0}
}
```

#### `asf⇥` async function
```js
async function (${1:arguments}) {
  ${0}
}
```

#### `iife⇥` immediately-invoked function expression (IIFE)
```js
;(function (${1:arguments}) {
  ${0}
})(${2})
```

#### `fa⇥` function apply
```js
${1:fn}.apply(${2:this}, ${3:arguments})
```

#### `fc⇥` function call
```js
${1:fn}.call(${2:this}, ${3:arguments})
```

#### `fb⇥` function bind
```js
${1:fn}.bind(${2:this}, ${3:arguments})
```

#### `af⇥` arrow function (ES6)
```js
(${1:arguments}) => ${2:statement}
```

#### `afb⇥` arrow function with body (ES6)
```js
(${1:arguments}) => {
  ${0}
}
```

#### `gf⇥` generator function (ES6)
```js
function* (${1:arguments}) {
  ${0}
}
```

#### `gfn⇥` named generator function (ES6)
```js
function* ${1:name}(${1:arguments}) {
  ${0}
}
```

### Iterables

#### `fe⇥` forEach loop
```js
${1:iterable}.forEach((${2:item}) => {
  ${0}
})
```

#### `map⇥` map function
```js
${1:iterable}.map((${2:item}) => {
  ${0}
})
```

#### `reduce⇥` reduce function
```js
${1:iterable}.reduce((${2:previous}, ${3:current}) => {
  ${0}
}${4:, initial})
```

#### `filter⇥` filter function
```js
${1:iterable}.filter((${2:item}) => {
  ${0}
})
```

#### `find⇥` ES6 find function
```js
${1:iterable}.find((${2:item}) => {
  ${0}
})
```

#### `every⇥` every function
```js
${1:iterable}.every((${2:item}) => {
  ${0}
})
```

#### `some⇥` some function
```js
${1:iterable}.some((${2:item}) => {
  ${0}
})
```

### Objects and classes

#### `cs⇥` class (ES6)
```js
class ${1:name} {
  constructor(${2:arguments}) {
    ${0}
  }
}
```

#### `csx⇥` extend a class (ES6)
```js
class ${1:name} extends ${2:base} {
  constructor(${2:arguments}) {
    super(${2:arguments})
    ${0}
  }
}
```

#### `:⇥` key/value pair
Javascript:
```js
${1:key}: ${2:'value'}
```
JSON:
```json
"${1:key}": ${2:"value"}
```

#### `m⇥` method (ES6 syntax)
```js
${1:method} (${2:arguments}) {
  ${0}
}
```

#### `get⇥` getter (ES6 syntax)
```js
get ${1:property} () {
  ${0}
}
```

#### `set⇥` setter (ES6 syntax)
```js
set ${1:property} (${2:value}) {
  ${0}
}
```

#### `gs⇥` getter and setter (ES6 syntax)
```js
get ${1:property} () {
  ${0}
}
set ${1:property} (${2:value}) {

}
```

#### `proto⇥` prototype method
```js
${1:Class}.prototype.${2:methodName} = function (${3:arguments}) {
  ${0}
}
```

#### `ok` Object.keys
```js
Object.keys(${1:obj})
```

#### `oa` Object.assign
```js
Object.assign(${1:dest}, ${2:source})
```

### Returning values

#### `re⇥` return
```js
return ${0}
```

#### `rth⇥` return this
```js
return this
```

#### `rn⇥` return null
```js
return null
```

#### `rt⇥` return true
```js
return true
```

#### `rf⇥` return false
```js
return false
```

#### `rp⇥` return Promise (ES6)
```js
return new Promise((resolve, reject) => {
  ${0}
})
```

#### `tof⇥` typeof comparison
```js
typeof ${1:source} === '${2:undefined}'
```

#### `iof⇥` instanceof comparison
```js
${1:source} instanceof ${2:Object}
```

#### `ia⇥` isArray
```js
Array.isArray(${1:source})
```

### Promises

#### `p⇥` new Promise (ES6)
```js
new Promise((resolve, reject) => {
  ${0}
})
```

#### `then⇥` Promise.then
```js
${1:promise}.then((${2:value}) => {
  ${0}
})
```

#### `catch⇥` Promise.catch
```js
${1:promise}.catch((${2:err}) => {
  ${0}
})
```

### ES6 modules

#### `e⇥` module export
```js
export ${1:member}
```

#### `ed⇥` module default export
```js
export default ${1:member}
```

#### `im⇥` module import
```js
import ${1:*} from '${2:module}'
```

#### `ia⇥` module import as
```js
import ${1:*} as ${2:name} from '${3:module}'
```

#### `id⇥` module import destructuring
```js
import {$1} from '${2:module}'
```

### BDD testing (Mocha, Jasmine, etc.)

#### `desc⇥` describe
```js
describe('${1:description}', function () {
  ${0}
})
```
#### `its⇥` synchronous "it"
```js
it('${1:description}', function () {
  ${0}
})
```
#### `ita⇥` asynchronous "it"
```js
it('${1:description}', function (done) {
  ${0}
})
```

#### `bf⇥` before test suite
```js
before(function () {
  ${0}
})
```

#### `bfe⇥` before each test
```js
beforeEach(function () {
  ${0}
})
```

#### `aft⇥` after test suite
```js
after(function () {
  ${0}
})
```

#### `afe⇥` after each test
```js
afterEach(function () {
  ${0}
})
```

### Timers

#### `st⇥` setTimeout
```js
setTimeout(() => {
  ${0}
}, ${1:delay})
```

#### `si⇥` setInterval
```js
setTimeout(() => {
  ${0}
}, ${1:delay})
```

#### `sim⇥` setInterval
```js
setImmediate(() => {
  ${0}
})
```

### DOM

#### `ae⇥` addEventListener
```js
${1:document}.addEventListener('${2:event}', ${3:ev} => {
  ${0}
})
```

#### `rel⇥` removeEventListener
```js
${1:document}.removeEventListener('${2:event}', ${3:listener})
```

#### `gi⇥` getElementById
```js
${1:document}.getElementById('${2:id}')
```

#### `gc⇥` getElementsByClassName
```js
Array.from(${1:document}.getElementsByClassName('${2:class}'))
```

#### `gt⇥` getElementsByTagName
```js
Array.from(${1:document}.getElementsByTagName('${2:tag}'))
```

#### `qs⇥` querySelector
```js
${1:document}.querySelector('${2:selector}')
```

#### `qsa⇥` querySelectorAll
```js
Array.from(${1:document}.querySelectorAll('${2:selector}'))
```

### `cdf⇥` createDocumentFragment

```js
${1:document}.createDocumentFragment(${2:elem});
```

### `cel⇥` createElement

```js
${1:document}.createElement(${2:elem});
```

### `ac⇥` appendChild

```js
${1:document}.appendChild(${2:elem});
```

### `rc⇥` removeChild

```js
${1:document}.removeChild(${2:elem});
```

### `cla⇥` classList.add

```js
${1:document}.classList.add('${2:class}');
```

### `ct⇥` classList.toggle

```js
${1:document}.classList.toggle('${2:class}');
```

### `clr⇥` classList.remove

```js
${1:document}.classList.remove('${2:class}');
```

### `ga⇥` getAttribute

```js
${1:document}.getAttribute('${2:attr}');
```

### `sa⇥` setAttribute

```js
${1:document}.setAttribute('${2:attr}', ${3:value});
```

### `ra⇥` removeAttribute

```js
${1:document}.removeAttribute('${2:attr}');
```

### Node.js

#### `cb⇥` Node.js style callback
```js
function (err, ${1:value}) {
  if (err) throw err
  t${0}
}
```

#### `r⇥` require a module
```js
require('${1:module}')
```
#### `cr⇥` require and assign a module
```js
const ${1:module} = require('${1:module}')
```

#### `em⇥` export member
```js
exports.${1:name} = ${2:value}
```

#### `me⇥` module.exports
```js
module.exports = ${1:name}
```

#### `on⇥` attach an event handler
```js
${1:emitter}.on('${2:event}', (${3:arguments}) => {
  ${0}
})
```

### Miscellaneous

#### `us⇥` use strict
```js
'use strict'
```

#### `js⇥` JSON Stringify
```js
JSON.stringify($0)
```

#### `jp⇥` JSON Parse
```js
JSON.parse($0)
```

#### `a⇥` await
```js
await ${0}
```

### Console

#### `cl⇥` console.log
```js
console.log(${0})
```

#### `ce⇥` console.error
```js
console.error(${0})
```

#### `cw⇥` console.warn
```js
console.warn(${0})
```

# License

The MIT License (MIT)

Copyright (c) 2016, [Jiří Špác](http://github.com/capaj)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NON INFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.