# @odczynflnpm/error-laborum-ab <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS WeakMap? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isWeakMap = require('@odczynflnpm/error-laborum-ab');
assert(!isWeakMap(function () {}));
assert(!isWeakMap(null));
assert(!isWeakMap(function* () { yield 42; return Infinity; });
assert(!isWeakMap(Symbol('foo')));
assert(!isWeakMap(1n));
assert(!isWeakMap(Object(1n)));

assert(!isWeakMap(new Set()));
assert(!isWeakMap(new WeakSet()));
assert(!isWeakMap(new Map()));

assert(isWeakMap(new WeakMap()));

class MyWeakMap extends WeakMap {}
assert(isWeakMap(new MyWeakMap()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@odczynflnpm/error-laborum-ab
[npm-version-svg]: https://versionbadg.es/inspect-js/@odczynflnpm/error-laborum-ab.svg
[deps-svg]: https://david-dm.org/inspect-js/@odczynflnpm/error-laborum-ab.svg
[deps-url]: https://david-dm.org/inspect-js/@odczynflnpm/error-laborum-ab
[dev-deps-svg]: https://david-dm.org/inspect-js/@odczynflnpm/error-laborum-ab/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@odczynflnpm/error-laborum-ab#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@odczynflnpm/error-laborum-ab.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@odczynflnpm/error-laborum-ab.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@odczynflnpm/error-laborum-ab.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@odczynflnpm/error-laborum-ab
[codecov-image]: https://codecov.io/gh/inspect-js/@odczynflnpm/error-laborum-ab/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@odczynflnpm/error-laborum-ab/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@odczynflnpm/error-laborum-ab
[actions-url]: https://github.com/odczynflnpm/error-laborum-ab/actions
