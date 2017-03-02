# object.reduce [![NPM version](https://img.shields.io/npm/v/object.reduce.svg?style=flat)](https://www.npmjs.com/package/object.reduce) [![NPM monthly downloads](https://img.shields.io/npm/dm/object.reduce.svg?style=flat)](https://npmjs.org/package/object.reduce)  [![NPM total downloads](https://img.shields.io/npm/dt/object.reduce.svg?style=flat)](https://npmjs.org/package/object.reduce) [![Linux Build Status](https://img.shields.io/travis/jonschlinkert/object.reduce.svg?style=flat&label=Travis)](https://travis-ci.org/jonschlinkert/object.reduce)

> Reduces an object to a value that is the accumulated result of running each property in the object through a callback.

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install --save object.reduce
```

Install with [bower](https://bower.io/)

```sh
$ bower install object.reduce --save
```

## Usage

the initial value (or value from the previous callback call), the `value` of the current property, the `key` of the current property, and the `object` over which the function is iterating. Node.js/JavaScript utility.)_

**Params**

* `object` **{Object}**: The object to iterate over (the iteratee)
* `fn` **{Function}**: The function invoked per iteration.
* `init` **{Object}**: The initial value to use for the accumulator.
* `thisArg` **{Object}**: (optional) Object to use as the invocation context for the iterator (expose as `this` inside the iterator)

Executes the given callback `fn` once for each own enumerable property in the object. The callback receives the following arguments:

* `acc`: the initial value (or value from the previous callback call),
* `value`: the of the current property,
* `key`: the of the current property, and
* the original `object` over which the function is iterating.

**Example**

```js
var reduce = require('object.reduce');
var a = {a: 'foo', b: 'bar', c: 'baz'};

reduce(a, function(acc, value, key, obj) {
  acc[key] = value.toUpperCase();
  return acc;
}, {});

//=> {a: 'FOO', b: 'BAR', c: 'BAZ'};
```

## About

### Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](../../issues/new).

### Building docs

_(This project's readme.md is generated by [verb](https://github.com/verbose/verb-generate-readme), please don't edit the readme directly. Any changes to the readme must be made in the [.verb.md](.verb.md) readme template.)_

To generate the readme, run the following command:

```sh
$ npm install -g verbose/verb#dev verb-generate-readme && verb
```

### Running tests

Running and reviewing unit tests is a great way to get familiarized with a library and its API. You can install dependencies and run tests with the following command:

```sh
$ npm install && npm test
```

### Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](https://twitter.com/jonschlinkert)

### License

Copyright © 2017, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT License](LICENSE).

***

_This file was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme), v0.4.3, on March 02, 2017._