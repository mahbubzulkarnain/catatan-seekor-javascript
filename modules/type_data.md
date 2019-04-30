# [Catatan Seekor: **JAVASCRIPT**](https://github.com/mahbubzulkarnain/catatan-seekor-javascript) / Type Data
##### by Mahbub Zulkarnain

## Table of Contents
* Type Data
* [Variables](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/variables.md)
* [Function](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/function.md)
* [Conditional](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/conditional.md)
* [Looping](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/looping.md)
* [Tips and Tricks](https://github.com/mahbubzulkarnain/catatan-seekor-javascript/blob/master/modules/tips_and_tricks.md)
* [Links](#links)
* [Forum](#forum)
* [Course](#course)

### String
```javascript
iniString = 'Type Data String';
iniString = "Type Data String";
iniString = `Type Data String`;
```
```javascript
console.log(typeof iniString) // string
```

### Number
```javascript
iniNumber = 0;
iniNumber = 0.1;
iniNumber = 1337e1;                  // 13370
iniNumber = 1337e-2;                 // 13.37
iniNumber = Number.MAX_VALUE;        // 1.7976931348623157e+308
iniNumber = Number.MIN_VALUE;        // 5e-324
iniNumber = Number.MAX_SAFE_INTEGER; // 9007199254740991
iniNumber = Number.MIN_SAFE_INTEGER; // -9007199254740991
```
```javascript
console.log(typeof iniNumber); // number
```

### Boolean
```javascript
iniBoolean = true;
iniBoolean = false;
```
```javascript
console.log(typeof iniBoolean); // boolean
```

### Function
```javascript
iniFunction = function() {};
iniFunction = () => {};
```
```javascript
console.log(typeof iniFunction); // function
console.log(iniFunction instanceof Function); // true
```

### Array
```javascript
iniArray = [];
```
```javascript
console.log(typeof iniArray); // object
console.log(iniArray instanceof Array); // true
```
```javascript
let data = [ "a", "b", "c"];

console.log(data[0]) // 'a'
console.log(data[data.length - 1]) // 'c'
```

### Object
```javascript
iniObject = {};
```
```javascript
console.log(typeof iniObject); // object
console.log(iniObject instanceof Object); // true
```
```javascript
let data = {
  a: "ini a",
  b: "ini b",
  c: "ini c",
}

console.log(data.a) // 'ini a'
console.log(data['a']) // 'ini a'
console.log(data); // { a: 'ini a', b: 'ini b', c: 'ini c' }

const { b, c } = data;
console.log( b ); // 'ini b'
console.log( c ); // 'ini c'

console.log(Object.keys(data)); // [ 'a', 'b', 'c' ]
console.log(Object.values(data)); // [ 'ini a', 'ini b', 'ini c' ]

```
```javascript
let dataBefore = {
  a: 'ini a',
  b: 'ini b',
  c: 'ini c',
}

let dataAfter = {
  ...dataBefore,
  ['a'] : 'ini a telah di update',
  ['c'] : dataBefore['c'] + ' telah di update juga',
  d : '5'
}

console.log({
  ...dataAfter,
  d : +dataAfter.d + 5 
}); // { a: 'ini a telah di update', b: 'ini b', c: 'ini c telah di update juga', d: 10 }
```

### Null
```javascript
iniNull = null;
```
```javascript
console.log(typeof iniNull); // object
```

### Undefined
```javascript
iniUndefined = undefined;
```
```javascript
console.log(typeof iniUndefined); // undefined
```
