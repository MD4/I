# i
[![NPM Version](https://img.shields.io/npm/v/i-.svg)](https://www.npmjs.com/package/i-)
[![Build Status](https://travis-ci.org/MD4/i.svg?branch=master)](https://travis-ci.org/MD4/i)
[![Dependency Status](https://david-dm.org/MD4/i.svg)](https://david-dm.org/MD4/i)
[![devDependency Status](https://david-dm.org/MD4/i/dev-status.svg)](https://david-dm.org/MD4/i#info=devDependencies)
[![Coverage Status](https://coveralls.io/repos/github/MD4/i/badge.svg?branch=master)](https://coveralls.io/github/MD4/i?branch=master)

A (very) simple library to expose only clones of referenced objects in function arguments.

## Installation

```npm install i-```

## Usage

### Require

```javascript
var i = require('i-');
// or simply
require('i-');
```

### Example

```javascript
var a = { a: 1, b: 2 };

var transform = (obj => {
  obj.b = 3;
  return obj;
}).i;

// or

transform = i(obj => {
  obj.b = 3;
  return obj;
});

// or

transform = i(function(obj) {
  obj.b = 3;
  return obj;
});

// or

transform = function(obj) {
  obj.b = 3;
  return obj;
}.i;

console.log(a);
console.log(transform(a));
console.log(a);
```

## test
```npm test```

## Notes

I still have no idea if it is a stupid or good idea.
