[![npm](https://img.shields.io/npm/v/start-start-preset.svg?style=flat-square)](https://www.npmjs.com/package/start-start-preset)
[![travis](http://img.shields.io/travis/start-runner/start-preset.svg?style=flat-square)](https://travis-ci.org/start-runner/start-preset)
[![deps](https://img.shields.io/gemnasium/start-runner/start-preset.svg?style=flat-square)](https://gemnasium.com/start-runner/start-preset)

Start preset for Start.

![](http://funkyimg.com/i/27yzy.gif)

## Install

```
npm i -D start-start-preset
```

## Usage

### Simple

```js
// package.json
"devDependencies": {
  "start": "3.x.x",
  "start-start-preset": "0.x.x"
},
"scripts": {
  "task": "babel-node node_modules/.bin/start start-start-preset",
  "build": "npm run task build",
  "dev": "npm run task dev",
  "lint": "npm run task lint",
  "test": "npm run task test",
  "tdd": "npm run task tdd",
  "cover": "npm run task cover",
  "travis": "npm run task travis"
}
```

### Extend

```js
// tasks.js
import start from 'start-start-preset';

export * from 'start-start-preset';

export function myTask() {
    return start(
        ...
    );
}
```

<sup>* example is rely on [babel-plugin-transform-export-extensions](https://babeljs.io/docs/plugins/transform-export-extensions/) from [babel-preset-stage-1](https://babeljs.io/docs/plugins/preset-stage-1/)</sup>

```js
// package.json
"devDependencies": {
  "start": "3.x.x",
  "start-start-preset": "0.x.x"
},
"scripts": {
  "task": "babel-node node_modules/.bin/start ./tasks",
  "build": "npm run task build",
  "dev": "npm run task dev",
  "lint": "npm run task lint",
  "test": "npm run task test",
  "tdd": "npm run task tdd",
  "cover": "npm run task cover",
  "travis": "npm run task travis",
  "my-task": "npm run task myTask"
}
```
