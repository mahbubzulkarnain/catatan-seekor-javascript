# Data Types

## Number

```javascript
iniNumber = 0;
iniNumber = 0.1;
iniNumber = 1337e1;                  // 13370
iniNumber = 1337e-2;                 // 13.37
iniNumber = 1337*1e-3;               // 1.337
iniNumber = Number.MAX_VALUE;        // 1.7976931348623157e+308
iniNumber = Number.MIN_VALUE;        // 5e-324
iniNumber = Number.MAX_SAFE_INTEGER; // 9007199254740991
iniNumber = Number.MIN_SAFE_INTEGER; // -9007199254740991
```

```javascript
console.log(typeof iniNumber); // number
```

## String

```javascript
iniString = 'Type Data String';
iniString = "Type Data String";
iniString = `Type Data String`;
```

```javascript
console.log(typeof iniString) // string
```

```javascript
let hours = ('0' + 1).slice(-2);  
let minutes = ('0' + 37).slice(-2);

console.log(`${hours}:${minutes} AM`); // '01:37 AM'
```

## Boolean

```javascript
iniBoolean = true;
iniBoolean = false;
```

```javascript
console.log(typeof iniBoolean); // boolean
```

## Function

```javascript
iniFunction = function() {};
iniFunction = () => {};
```

```javascript
console.log(typeof iniFunction); // function
console.log(iniFunction instanceof Function); // true
```

## Array

```javascript
iniArray = [];
```

```javascript
console.log(typeof iniArray); // object
console.log(iniArray instanceof Array); // true
console.log(Array.isArray(iniArray)); // true
```

```javascript
let data = [ "a", "b", "c"];

console.log(data[0]) // 'a'
console.log(data[data.length - 1]) // 'c'
```

```javascript
let data = [ 0, 1, 2, 3, 4 ];
console.log(
  data.indexOf( 2 )
); // 2
console.log(
  data.indexOf( 10 )
); // -1
```

```javascript
let data = [ 0, 1, 2, 3, 4 ];
console.log(
    data.includes( 2 )
); // true
console.log(
    data.includes( 10 )
); // false
```

```javascript
let data = [ 0, 1, 2, 3, 4 ];

console.log(
  data.filter((item, index) => {
    return item !== 0 && index !== (data.length - 1);
  })
); // [ 1, 2, 3 ]
```

```javascript
let data = Array.of( 0, 1, 2, 3, 4 );
console.log( data ); // [ 0, 1, 2, 3, 4 ]
```

```javascript
let data = [];

(new Array(5).fill()).forEach((item, index)=> {
  data.push(index)
})

console.log( data ) // [ 0, 1, 2, 3, 4]
```

```javascript
console.log(
  (new Array(5).fill('')).map((item, index)=> {
    return index;
  })
); // [ 0, 1, 2, 3, 4 ]
```

## Object

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

```javascript
let data = {
  name: ['Name is required.'],
  email: ['Email is required.'],
  password: ['Password is required.'],
};

for (const [key, value] of Object.entries(data)) {
  console.log(value[0]);
};

// Output:
// Name is required.
// Email is required.
// Password is required.
```

## Null

```javascript
iniNull = null;
```

```javascript
console.log(typeof iniNull); // object
```

## Undefined

```javascript
iniUndefined = undefined;
```

```javascript
console.log(typeof iniUndefined); // undefined
```

