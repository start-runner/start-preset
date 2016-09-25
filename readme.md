# start-start-preset

[![npm](https://img.shields.io/npm/v/start-start-preset.svg?style=flat-square)](https://www.npmjs.com/package/start-start-preset)
[![travis](http://img.shields.io/travis/start-runner/start-preset.svg?style=flat-square)](https://travis-ci.org/start-runner/start-preset)
[![deps](https://img.shields.io/gemnasium/start-runner/start-preset.svg?style=flat-square)](https://gemnasium.com/start-runner/start-preset)

Start preset for [Start](https://github.com/start-runner/start).

![recursion](pic.gif)

## Install

```
npm i -D start-start-preset
```

## Usage

See [documentation](https://github.com/start-runner/start#readme) and [source tasks file](lib/index.js) for details.

### Simple

```
npm i -D start-babel-cli start-start-preset
```

```js
// package.json
"scripts": {
  "start": "start-runner -p start-start-preset"
}
```

Available commands:

```
npm start build
npm start dev
npm start lint
npm start test
npm start tdd
npm start coverage
npm start ci
```

### Extend

```js
// tasks.js
import start from 'start-start-preset';

export * from 'start-start-preset';

export const myTasksRunner = () => start(
    ...
);
```

<sup>* example is rely on [babel-plugin-transform-export-extensions](https://babeljs.io/docs/plugins/transform-export-extensions/) from [babel-preset-stage-1](https://babeljs.io/docs/plugins/preset-stage-1/)</sup>

```
npm i -D start-babel-cli start-start-preset
```

```js
// package.json
"scripts": {
  "start": "start-runner -f ./tasks"
}
```

Available commands:

```
npm start build
npm start dev
npm start lint
npm start test
npm start tdd
npm start coverage
npm start ci
npm start myTasksRunner
```
