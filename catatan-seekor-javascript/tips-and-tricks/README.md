# Tips and Tricks

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

## Convert

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

