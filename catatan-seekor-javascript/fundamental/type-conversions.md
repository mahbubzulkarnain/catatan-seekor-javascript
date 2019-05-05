# Type Conversions

#### To String

```javascript
let data = true; // boolean
let data = 0; // number

iniString = String( data );
iniString = data + '';
iniString = data.toString();

console.log( typeof iniString ); // string
```

#### To Number

```javascript
let data = true; // boolean
let data = '0'; // string

iniNumber = Number( data );
iniNumber = +data;

console.log( typeof iniNumber ); // number
```

#### To Boolean

```javascript
let data = '0'; // string
let data = 0; // number

iniBoolean = Boolean( data );
iniBoolean = !!+data;

console.log( typeof iniBoolean ); // boolean
```

