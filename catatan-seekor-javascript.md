---
description: 'Brendan Eich ( July 4, 1961 )'
---

# Catatan Seekor: JAVASCRIPT

## Type Data

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

### String

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
  data.indexOf( 10 )
); // -1
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

### VAR \( Global \)

```javascript
var iniVariableGlobal = TYPE_DATA;
```

### LET \( Local \)

```javascript
let iniVariableGlobal = TYPE_DATA;
```

### CONST \( Read Only \)

```javascript
let iniVariableGlobal = TYPE_DATA;
```

### Assignment Operator

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

### The _if_ Statement

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

### The _else_ Statement

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

### The _else if_ Statement

```javascript
const condition = false;
const condition2 = true;
const isTrue = 'text true';
const isFalse = 'text false';

console.log((() => {
  if (condition) return isTrue; 
  else if (condition2) return 'else if true'; 
  else return isFalse;
})()); // 'else if true'

console.log((() => {
  return condition 
  ? isTrue 
  : condition2 
    ? 'else if true'
    : isFalse
})()); // 'else if true'
```

### The _switch case_ Statement

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

### The _try catch finally_ Statement

```javascript
try {
  // tryCode - Block of code to try
}
catch(err) {
  // catchCode - Block of code to handle errors
} 
finally {
  // finallyCode - Block of code to be executed regardless of the try / catch result
}
```

source [https://www.w3schools.com/jsref/jsref\_try\_catch.asp](https://www.w3schools.com/jsref/jsref_try_catch.asp)

```javascript
const isError = true;
let message = '';

try {
  if( isError ) throw 'throw from block try';
  message += 'from block try. ';
}
catch (e) {
  message += `from block catch, with message: "${e}". `;
}
finally {
  message += 'from block finally. ';
}

console.log(message); // from block catch, with message: "throw from block try". from block finally.
```

## Looping

### The _for_ Statement

```javascript
let input = ['t','','r','','u','','e','1','2'];

console.log((() => {
  let output = "";
  for (let i = 0; i < input.length; i++){
    if( input[i] === '') continue;
    if( output.length > 3) break;
    output += input[i];
  } 
  return output
})()); // 'true'
```

### The _while_ Statement

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

### The _do while_ Statement

```javascript
let input = ['t','r','u','e'];

console.log((() => {
  let output = ""; let i = 0;
  do {
    output += input[i];
    i++;
  } while(i < input.length) 
  return output
})()); // 'true'
```

## Tips and Tricks

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

### RegExp

```javascript
// validation email
const email = /^(([^<>()[\]\\.,;:\s@\"]+(\.[^<>()[\]\\.,;:\s@\"]+)*)|(\".+\"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
console.log(email.test('mahbubzulkarnain@domain.com')); // true
```

```javascript
// validation password
// Min 6 characters which contain at least one numeric digit, one uppercase letter, one lowercase letter, and one special character
const password = /^(?=.*\d)(?=.*[A-Z])(?=.*[a-z])(?=.*[^a-zA-Z0-9])(?!.*\s).{6,}$/;
console.log(password.test('Mahbub!23')); // true
```

```javascript
// validation url
const url = /^(http:\/\/www\.|https:\/\/www\.|http:\/\/|https:\/\/)?[a-z0-9]+([-.]{1}[a-z0-9]+)*\.[a-z]{2,5}(:[0-9]{1,5})?(\/.*)?$/;
console.log(url.test('https://github.com/mahbubzulkarnain')); // true
```

```javascript
// validation username
const username = /(^[a-zA-Z][a-zA-Z0-9._]+[a-zA-Z0-9]).{6,}$/g;
console.log(username.test('mahbubzulkarnain')); // true
```

## Course

* [Hacktiv8 Indonesia](https://hacktiv8.com)

## Forum

### Telegram

* [JavaScript Indonesia Channel](https://t.me/Indonesia_Javascript)

## Links

### Docs

* [Angular](https://angular.io/guide/quickstart)
* [Apollo](https://www.apollographql.com/docs)
* [Certbot](https://certbot.eff.org/docs/)
* [Expo](https://docs.expo.io/versions/latest)
* [Express JS](https://expressjs.com/en/starter/installing.html)
* [GraphQL](https://graphql.org/code/#javascript)
* [Native Base](https://docs.nativebase.io)
* [PM2](https://pm2.io/doc/en/runtime/overview)
* [React JS](https://reactjs.org/docs/getting-started.html)
* [React Native](https://facebook.github.io/react-native/docs/getting-started)
* [Redis](https://redis.io/documentation)

### Github

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
* [The Book of Secret Knowledge](https://github.com/trimstray/the-book-of-secret-knowledge) by trimstray
* [Web Developer Shortcut](https://github.com/rkukuh/web-developer-shortcut) by rkukuh

### NPM

Dependencies

* [Apollo Boost](https://www.npmjs.com/package/apollo-boost)
* [Axios](https://www.npmjs.com/package/axios)
* [Bcrypt](https://www.npmjs.com/package/bcrypt)
* [Cors](https://www.npmjs.com/package/cors)
* [D3 Interpolate](https://www.npmjs.com/package/d3-interpolate)
* [Express Validator](https://www.npmjs.com/package/express-validator)
* [Firebase](https://www.npmjs.com/package/firebase)
* [Form Data](https://www.npmjs.com/package/form-data)
* [Internet Printing Protocol \(IPP\) for nodejs](https://www.npmjs.com/package/ipp)
* [JSONWebToken \(JWT\)](https://www.npmjs.com/package/jsonwebtoken)
* [JSPDF](https://www.npmjs.com/package/jspdf)
* [Lodash](https://www.npmjs.com/package/lodash)
* [Moment](https://www.npmjs.com/package/moment)
* [Mongoose](https://www.npmjs.com/package/mongoose)
* [Node Printer](https://www.npmjs.com/package/node-printer) for Local Only
* [Passport](https://www.npmjs.com/package/passport)
* [QRCode](https://www.npmjs.com/package/qrcode)
* [React Redux](https://www.npmjs.com/package/react-redux)
* [React Native Render HTML](https://www.npmjs.com/package/react-native-render-html)
* [React Native QRCode](https://www.npmjs.com/package/react-native-qrcode)
* [React Navigation](https://www.npmjs.com/package/react-navigation)
* [Redux](https://www.npmjs.com/package/redux)
* [Redux Thunk](https://www.npmjs.com/package/redux-thunk)
* [Sequelize](https://www.npmjs.com/package/sequelize)

DevDependencies

* [Chai](https://www.npmjs.com/package/chai)
* [Chai HTTP](https://www.npmjs.com/package/chai-http)
* [Dotenv](https://www.npmjs.com/package/dotenv)
* [Mocha](https://www.npmjs.com/package/mocha)
* [NYC](https://www.npmjs.com/package/nyc)

### Website

* [Free Code Camp](https://www.freecodecamp.org)
* [Javascripting](https://www.javascripting.com) \( List of Javascript Library \)
* [Regex Lib](http://regexlib.com)
* [Sabe](https://sabe.io/classes/javascript)
* [Skptricks](https://www.skptricks.com/search/label/javascript)
* [W3Schools](https://www.w3schools.com/jsref/default.asp)

### Youtube

* [Dasar Pemrograman dengan Javascript](https://www.youtube.com/playlist?list=PLFIM0718LjIWXagluzROrA-iBY9eeUt4w) by Web Programming UNPAS
* [JavaScript Tutorials for Beginners](https://www.youtube.com/playlist?list=PL4cUxeGkcC9i9Ae2D9Ee1RvylH38dKuET) by The Net Ninja
* [Modern JavaScript Tutorial](https://www.youtube.com/playlist?list=PL4cUxeGkcC9haFPT7J25Q9GRB_ZkFrQAc) by The Net Ninja

## Testing

* [Burp Suite](https://portswigger.net/burp)
* [K6](https://k6.io)
* [Load Impact](https://loadimpact.com)
* [New Relic](https://newrelic.com)
* [Security Headers](https://securityheaders.com)
* [Sn1per](https://github.com/1N3/Sn1per) by 1N3
* [Snyk](https://snyk.io)
* [Storybook](https://storybook.js.org)

