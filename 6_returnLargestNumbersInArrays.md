## Return Largest Numbers in Arrays :
### Return an array consisting of the largest number from each provided sub-array. For simplicity, the provided array will contain exactly 4 sub-arrays.

```javascript
function largestOfFour(arr) {
  var newArr = [];

  for(var i = 0; i < arr.length; i++) {
    var total = 0;
      for(var j = 0; j < arr.length; j++){
        if(Math.max(arr[i][j]) > total)
          total = Math.max(arr[i][j]);
      }
      newArr.push(total);
    }
      return newArr;
  }
largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

<details>
  <p>Having two for loops to iterate through the arrays. Under the first for loop we have a total. </p>
  <p> We use  Math.max to see if it's greater than total... if it is then total equal's Math.max </p>
  <p> lastly we push the toal to newArr </p>
</details>
