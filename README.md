# tslint-formatter-beauty

Beautiful TSLint custom formatter.

![](screenshot.png)

![Travis](https://img.shields.io/travis/g-plane/tslint-formatter-beauty.svg?style=flat-square)
![license](https://img.shields.io/github/license/g-plane/tslint-formatter-beauty.svg?style=flat-square)
![npm](https://img.shields.io/npm/v/tslint-formatter-beauty.svg?style=flat-square)
![npm](https://img.shields.io/npm/dm/tslint-formatter-beauty.svg?style=flat-square)

## Installation

Using Yarn:

```
yarn add --dev tslint-formatter-beauty
```

Using npm:

```
npm install --save-dev tslint-formatter-beauty
```

## Usage

### TSLint CLI:

```
tslint --formatters-dir ./node_modules/tslint-formatter-beauty -t beauty -p .
```

### gulp-tslint

```js
const gulp = require('gulp')
const tslint = require('gulp-tslint')

gulp.task('lint', () =>
  gulp.src('file.ts')
    .pipe(tslint({
      formattersDirectory: 'node_modules/tslint-formatter-beauty',
      formatter: 'beauty'
    }))
)
```

### tslint-loader

```js
module.exports = {
  // ... other options
  module: {
    rules: [
      // ... other options
      {
        test: /\.ts$/,
        exclude: /node_modules/,
        loader: 'tslint-loader',
        options: {
          formattersDirectory: 'node_modules/tslint-formatter-beauty',
          formatter: 'beauty'
        }
      }
    ]
  }
}
```

## License

Apache License 2.0

Copyright (c) 2018-present Pig Fang
