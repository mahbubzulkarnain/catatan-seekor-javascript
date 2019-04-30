# Catatan Seekor: **JAVASCRIPT**
##### by Mahbub Zulkarnain

## Table of Contents
* [Type data](#type-data)
* [Variables](#variables)
* [Function](#function-1)
* [Conditional](#conditional)
* [Looping](#looping)
* [Tips and Tricks](#tips-and-tricks)
* [Links](#links)

## Type Data

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


## Variables
### VAR ( Global )
```javascript
var iniVariableGlobal = TYPE_DATA;
```

### LET ( Local )
```javascript
let iniVariableGlobal = TYPE_DATA;
```

### CONST ( Read Only )
```javascript
let iniVariableGlobal = TYPE_DATA;
```

## Assignment Operator
```javascript
a  = 1;              // a = 1;
a += 1;              // a = a + 1;
a -= 1;              // a = a - 1;
a *= 1;              // a = a * 1;
a /= 1;              // a = a / 1;
a %= 1;              // a = a % 1;
```
```javascript
a  = 1 + 1;          //  1  + 1 = 2
b  = a + 1;          // (2) + 1 = 3
c  = a = b = 3;      // c = 3, a = 3, b = 3
d  = a += b /= c;    // ? 
```

## Function
```javascript
function introduction(name) {
  console.log(`Hai, my name is ${ name }.`);
};

introduction('Mahbub'); // 'Hai, my name is Mahbub.'
```
```javascript
function introduction({ firstName, lastName }) {
  console.log(`Hai, my name is ${ firstName } ${ lastName }.`);
};

introduction({firstName: 'Mahbub', lastName: 'Zulkarnain'}); // 'Hai, my name is Mahbub Zulkarnain.'
```
```javascript
function introduction({ name: { firstName, lastName }, hobby }) {
  console.log(`Hai, my name is ${ firstName } ${ lastName }. My favorite hobby is ${ hobby }.`);
};

introduction(
  {
    name: { firstName: 'Mahbub', lastName: 'Zulkarnain' },
    hobby: 'traveling'
  },
); // 'Hai, my name is Mahbub Zulkarnain. My favorite hobby is traveling.'
```

### Declaration
```javascript
// bisa di gunakan sebelum deklarasi function
console.log(iniFunctionDeclaration()); // 'tampil text ini'

// contoh : deklarasi "function declarations"
function iniFunctionDeclaration() {
  return "tampil text ini";
};

// bisa di gunakan sesudah deklarasi function
console.log(iniFunctionDeclaration()); // 'tampil text ini'
```

### Expression
```javascript
// tidak bisa di gunakan sebelum deklarasi function
console.log(iniFunctionExpressions()); // RefferenceError: iniFunctionExpressions is not defined

// contoh : deklarasi "function expressions"
var iniFunctionExpressions = function() {
  return "tampil text ini";
};

// OR

// contoh : deklarasi "function expressions"
var iniFunctionExpressions = () => {
  return "tampil text ini";
};

// bisa di gunakan sesudah deklarasi function
console.log(iniFunctionExpressions()); // 'tampil text ini'
```

### Async/Await
```javascript
async function asyncFunction() {
  return 'ini function async';
}

asyncFunction().then(console.log); // 'ini function async'
```
```javascript
async function asyncFunction() {
  return 'ini function async';
};

(async () => {
  try {
    console.log(await asyncFunction());    
  } catch (e) {
    console.log(e.message);
  }
})(); // 'ini function async'
```

## Conditional
### Comparison and Logical Operator
```javascript
const conditional = !false // true
```
```javascript
let dataIsNotEmpty = '';
let dataIsNotEmpty = 0;
let dataIsNotEmpty = null;
let dataIsNotEmpty = undefined;

console.log(!dataIsNotEmpty);           // true
console.log(!!dataIsNotEmpty);          // false
console.log(!!!dataIsNotEmpty);         // true
console.log(!!!!!!!!!!dataIsNotEmpty);  // ?
```
```javascript
console.log(0 == 0);                    // true
console.log(0 == '0');                  // true
console.log(0 != '0');                  // false
console.log(true != 'true');            // true
console.log(!(true != 'true'));         // false
```
```javascript
console.log(0 < -1);                    // false
console.log(-1 <= '-1');                // true
console.log(0 > '-2');                  // true
console.log(-1 >= -1);                  // true
console.log(true && !false);            // true
console.log(true || false);             // true
```
```javascript
console.log(0 === 0);                   // true
console.log(0 === '0');                 // false
console.log(0 !== '0');                 // true

console.log(!!+'1337');                 // true
console.log(!+'satu');                  // true
```

### The if Statement
```javascript
const condition = true;
const isTrue = 'text true';

console.log((() => {
  if (condition) return isTrue; 
})()); // 'text true'

console.log((() => {
  return (condition) && isTrue
})()); // 'text true'

console.log((() => {
  return (!condition) || isTrue
})()); // 'text true'
```

### The else Statement
```javascript
const condition = true;
const isTrue = 'text true';
const isFalse = 'text false';

console.log((() => {
  if (condition) return isTrue; 
  else return isFalse;
})()); // 'text true'

console.log((() => {
  return condition ? isTrue : isFalse
})()); // 'text true'
```

### The else if Statement
```javascript
const condition = true;
const condition2 = false;
const isTrue = 'text true';
const isFalse = 'text false';

console.log((() => {
  if (condition) return isTrue; 
  else if (condition2) return 'else if true'; 
  else return isFalse;
})()); // 'text true'
```

### The switch case Statement
```javascript
const condition = 1;
const isTrue = 'text true';
const isFalse = 'text false';


console.log((() => {
  let output;
  switch (condition) {
    case 0:
      output = isFalse;
      break;
    case 1:
    case 2:
      output = 'With case 2'
      break;
    default:
      output = "default";
      break;
  }
  return output;
})()); // 'With case 2'
```

## Looping
### The for Statement
```javascript
let input = ['t','r','u','e'];

console.log((() => {
  let output = "";
  for (let i = 0; i < input.length; i++){
    output += input[i];
  } 
  return output
})()); // 'true'
```

### The while Statement
```javascript
let input = ['t','r','u','e'];

console.log((() => {
  let output = ""; let i = 0;
  while(i < input.length){
    output += input[i];
    i++;
  } 
  return output
})()); // 'true'
```

## Tips and Tricks
### Convert
```javascript
// Convert number to rupiah
((number, isShowRp = true) => {
  return (isShowRp ? 'Rp': '') + Number
      .parseFloat(+number ? +number : 0)
      .toFixed(0)
      .toString()
      .replace(/\B(?=(\d{3})+(?!\d))/g, '.')
})(100000); // Rp100.000
```

### Random
```javascript
// Get random item from array
((data) => {
  return data[Math.floor(Math.random() * data.length)]
})(['1337', 'Random', 666, 'Mahbub', 10, 1993, 'Zulkarnain']);
```
```javascript
// Get random number with range
((min, max) => {
  return Math.floor(Math.random() * (max - min + 1)) + min;
})(1, 10);
```
```javascript
// Generate array of number with range
((min, max) => {
  let data = [];
  for (let i = min; data.push(i++) < max;);
  return data;
})(1, 10); 
```
```javascript
// Generate random string with specified length
((length) => {
  let data = '';
  for (; data.length < length; data += Math.random().toString(36).substr(2));
  return data.substr(0, length);
})(10);
```
```javascript
// Suffle an array of numbers
((data) => {
  return data.sort(() => Math.random() - 0.5);
})([ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 ]);
```

## Links
* [30 Seconds of Code](https://github.com/30-seconds/30-seconds-of-code) by 30-seconds
* [33 JS Concepts](https://github.com/leonardomso/33-js-concepts) by leonardomso
* [Clean Code Javascript](https://github.com/ryanmcdermott/clean-code-javascript) by ryanmcdermott
* [Google Cloud Node](https://github.com/googleapis/google-cloud-node) by googleapis
* [JavaScript Algorithms and Data Structures](https://github.com/trekhleb/javascript-algorithms) by trekhleb
* [Math as Code](https://github.com/Jam3/math-as-code) by Jam3
* [Modern JS Cheatsheet](https://github.com/mbeaudru/modern-js-cheatsheet) by mbeaudru
* [Nginx Admin's Handbook](https://github.com/trimstray/nginx-admins-handbook) by trimstray
* [Project Based Learning](https://github.com/tuvtran/project-based-learning) by tuvtran
* [Public APIs](https://github.com/toddmotto/public-apis) by toddmotto
* [Skptricks](https://www.skptricks.com)
* [The Book of Secret Knowledge](https://github.com/trimstray/the-book-of-secret-knowledge) by trimstray
* [Web Developer Shortcut](https://github.com/rkukuh/web-developer-shortcut) by rkukuh

## Forum
### Telegram
* [JavaScript Indonesia Channel](https://t.me/Indonesia_Javascript) 

## Course
* [Hacktiv8 Indonesia](https://hacktiv8.com)
