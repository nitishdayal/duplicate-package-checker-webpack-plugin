# duplicate-package-checker-webpack-plugin

[![NPM version][npm-image]][npm-url] [![Downloads][downloads-image]][npm-url] [![Build Status](https://travis-ci.org/darrenscerri/duplicate-package-checker-webpack-plugin.svg?branch=master)](https://travis-ci.org/darrenscerri/duplicate-package-checker-webpack-plugin)

Webpack plugin that warns you when multiple versions of the same package exist in a build.

![duplicate-package-checker-webpack-plugin](https://cloud.githubusercontent.com/assets/729230/21966496/c6809252-db74-11e6-91d5-73d13e07e615.png)

## Why?

It might be possible that a single package gets included multiple times in a Webpack build due to different package versions. This situation may happen without any warning,  resulting in extra bloat in your build and may lead to hard-to-find bugs.

This plugin will warn you of such cases to minimize build size and avoid bugs caused by unintended duplicate packages.

Motivation: https://github.com/webpack/webpack/issues/385 and https://github.com/webpack/webpack/issues/646.

## Install

```sh
npm install duplicate-package-checker-webpack-plugin --save-dev
```

## Configuration

Add the plugin to your webpack config:

```js
var DuplicatePackageCheckerPlugin = require('duplicate-package-checker-webpack-plugin');

module.exports = {
    plugins: [
      new DuplicatePackageCheckerPlugin()
    ]
};
```

[downloads-image]: https://img.shields.io/npm/dt/duplicate-package-checker-webpack-plugin.svg
[npm-url]: https://www.npmjs.com/package/duplicate-package-checker-webpack-plugin
[npm-image]: https://img.shields.io/npm/v/duplicate-package-checker-webpack-plugin.svg
