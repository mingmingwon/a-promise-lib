<a href="http://promisesaplus.com/">
  <img src="http://promisesaplus.com/assets/logo-small.png" alt="Promises/A+ Logo" title="Promises/A+" align="right" width="70px" />
</a>

[![npm](https://img.shields.io/npm/v/a-promise-lib.svg)](https://www.npmjs.com/package/a-promise-lib) [![npm](https://img.shields.io/npm/dt/a-promise-lib.svg)](https://www.npmjs.com/package/a-promise-lib) [![GitHub](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/mingmingwon/a-promise-lib/blob/master/LICENSE) 

# Introduction

An implementation of [Promises/A+](http://promisesaplus.com/) using ES6, and [Chinese specification](https://github.com/mingmingwon/a-promise-lib/blob/master/spec_cn.md) of Promises/A+.

# Install
[![NPM](https://nodei.co/npm/a-promise-lib.png)](https://nodei.co/npm/a-promise-lib/)

```node
npm i a-promise-lib
```
# Usage

```js
let Promise = require('a-promise-lib')

let promise = new Promise((resolve, reject) => {
  setTimeout(resolve, 1000, 'Success')
}).then(res => {
  console.log(res)
  return Promise.resolve('Yeah')
})

;(async () => {
  const ret = await promise
  console.log(ret)
})()
```

# API
This library has achieved all the APIs same as JavaScript Standard built-in [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise), including static methods:

- `Promise.resolve`
- `Promise.reject`
- `Promise.all`
- `Promise.race`

and prototype methods:

- `Promise.prototype.then`
- `Promise.prototype.catch`
- `Promise.prototype.finally`

and others:

- `Promise.deferred`
- `Promise.prototype.done`

# Compliances Test

Refer to [Promises/A+ Compliance Test Suite](https://github.com/promises-aplus/promises-tests).

```node
npm run test
```

Result like this:

```bash
872 passing (17s)
```

# License

The MIT License
