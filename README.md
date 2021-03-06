# filter-values [![NPM version](https://badge.fury.io/js/filter-values.svg)](http://badge.fury.io/js/filter-values)  [![Build Status](https://travis-ci.org/jonschlinkert/filter-values.svg)](https://travis-ci.org/jonschlinkert/filter-values)

> Filter an object values using glob patterns or with a `callback` function returns true.

Install with [npm](https://www.npmjs.com/)

```sh
$ npm i filter-values --save
```

## Usage

```js
var filter = require('filter-values');

filter({a: 'a', b: 'b', c: 'c'}, function(value, key, obj) {
  return key !== 'b';
});
//=> {a: 'a', c: 'c'}

filter({a: 'a', b: 'b', c: 'c'}, function(value, key, obj) {
  return key === 'b';
});
//=> {b: 'b'}

filter({a: 'a', b: 'b', c: 'c'}, function(value, key, obj) {
  return value === 'b';
});
//=> {b: 'b'}

filter({a: 'a', b: 'bbd', c: 'bca2'}, ['b*', '!bc*'])
//=> {b: 'bbd'}

filter({a: 'a', b: 'bbd', c: 'bca2'}, '!b*')
//=> {a: 'a'}
```

## Related

* [filter-object](https://www.npmjs.com/package/filter-object): Return a copy of an object, filtered to have only keys that match the given… [more](https://www.npmjs.com/package/filter-object) | [homepage](https://github.com/jonschlinkert/filter-object)
* [micromatch](https://www.npmjs.com/package/micromatch): Glob matching for javascript/node.js. A drop-in replacement and faster alternative to minimatch and multimatch. Just… [more](https://www.npmjs.com/package/micromatch) | [homepage](https://github.com/jonschlinkert/micromatch)
* [rename-keys](https://www.npmjs.com/package/rename-keys): Modify the names of the own enumerable properties (keys) of an object. | [homepage](https://github.com/jonschlinkert/rename-keys)
* [sort-object](https://www.npmjs.com/package/sort-object): Sort the keys in an object. | [homepage](https://github.com/doowb/sort-object)

## Running tests

Install dev dependencies:

```sh
$ npm i -d && npm test
```

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/filter-values/issues/new).

## Author

**Jon Schlinkert**

+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright © 2014-2015 [Jon Schlinkert](https://github.com/jonschlinkert)
Released under the MIT license.

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on September 08, 2015._
