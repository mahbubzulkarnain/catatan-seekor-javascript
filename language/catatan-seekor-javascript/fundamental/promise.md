# Promise

```javascript
const isError = true;

(new Promise(((resolve, reject) => {
  setTimeout(() => {
    if (!isError) {
      resolve('Fullfilled');
    } else {
      reject('Rejected');
    }
  }, 1000);
  
  console.log('Pending');
})))
  .then((response) => {
    console.log(response);  // Fullfilled
  })
  .catch((error) => {
    console.log(error);     // Rejected
  })
  .finally(() => {
    console.log('Settled');
  });

// Output:
// Pending
// Rejected
// Settled
```

