## Chunky Monkey
<p> Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.</p>

```javascript
function chunkArrayInGroups(arr, size) {
  // store array
  var newArr = [];
  while(arr.length > 0) {
  // use the .splice()
    newArr.push(arr.splice(0, size));
  }
  return newArr;
}
chunkArrayInGroups(["a", "b", "c", "d"], 2);
```

<details> 
  <p>Since using the **.splice()** method, we destroy the array ['a', 'b']. We then use the **.push()** to push what we destroyed and split it up into a two-dimensional array.  </p>
</details>
