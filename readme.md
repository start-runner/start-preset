# start-start-preset

[![npm](https://img.shields.io/npm/v/start-start-preset.svg?style=flat-square)](https://www.npmjs.com/package/start-start-preset)
[![travis](http://img.shields.io/travis/start-runner/start-preset.svg?style=flat-square)](https://travis-ci.org/start-runner/start-preset)
[![deps](https://img.shields.io/gemnasium/start-runner/start-preset.svg?style=flat-square)](https://gemnasium.com/start-runner/start-preset)
[![gitter](https://img.shields.io/badge/gitter-join_chat_%E2%86%92-00d06f.svg?style=flat-square)](https://gitter.im/start-runner/start)

Start preset for [Start](https://github.com/start-runner/start).

![](http://funkyimg.com/i/27yzy.gif)

## Install

```
npm i -D start-start-preset
```

## Usage

See [documentation](https://github.com/start-runner/start#readme) and [source tasks file](lib/index.js) for details.

### Simple

```js
// package.json
"devDependencies": {
  "start-babel-cli": "0.x.x",
  "start-start-preset": "1.x.x"
},
"scripts": {
  "start": "start start-start-preset"
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

export function myTasksRunner() {
    return start(
        ...
    );
}
```

<sup>* example is rely on [babel-plugin-transform-export-extensions](https://babeljs.io/docs/plugins/transform-export-extensions/) from [babel-preset-stage-1](https://babeljs.io/docs/plugins/preset-stage-1/)</sup>

```js
// package.json
"devDependencies": {
  "start-babel-cli": "0.x.x",
  "start-start-preset": "1.x.x"
},
"scripts": {
  "start": "start ./tasks"
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
