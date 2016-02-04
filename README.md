[![npm](https://img.shields.io/npm/v/start-start-pack.svg?style=flat-square)](https://www.npmjs.com/package/start-start-pack)
[![travis](http://img.shields.io/travis/start-runner/start-pack.svg?style=flat-square)](https://travis-ci.org/start-runner/start-pack)
[![deps](https://img.shields.io/gemnasium/start-runner/start-pack.svg?style=flat-square)](https://gemnasium.com/start-runner/start-pack)

Start pack for Start.

![](http://funkyimg.com/i/27xdm.jpg)

## Install

```
npm i -D start-start-pack
```

## Usage

```js
// package.json
"scripts": {
  "task": "babel-node node_modules/.bin/start start-start-pack",
  "build": "npm run task build",
  "dev": "npm run task dev",
  "lint": "npm run task lint",
  "test": "npm run task test",
  "tdd": "npm run task tdd",
  "cover": "npm run task cover",
  "travis": "npm run task travis"
}
```
