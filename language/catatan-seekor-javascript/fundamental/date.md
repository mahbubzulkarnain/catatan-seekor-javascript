# Date

```javascript
let now = new Date();

console.log(now);                       // 1970-01-01T00:00:00.000Z

console.log(now.toISOString());         // 1970-01-01T00:00:00.000Z
console.log(now.toUTCString());         // Thu, 01 Jan 1970 00:00:00 GMT

console.log(now.toDateString());        // Thu Jan 01 1970
console.log(now.toTimeString());        // 07:00:00 GMT+0700 (Western Indonesia Time)

console.log(now.toLocaleString());      // 1/1/1970, 7:00:00 AM
console.log(now.toLocaleDateString());  // 1/1/1970
console.log(now.toLocaleTimeString());  // 7:00:00 AM

console.log(now.toJSON());              // 1970-01-01T00:00:00.000Z
console.log(now.toString());            // Thu Jan 01 1970 07:00:00 GMT+0700 (Western Indonesia Time)

console.log(now.getTime());             // 25200000
```

 

