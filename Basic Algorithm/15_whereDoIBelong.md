## Where Do I Belong
<p>Return the lowest index at which a value (second argument) should be inserted into an array (first argument) once it has been sorted. The returned value should be a number. </p>

```javascript
function getIndexToIns(arr, num) {
 arr.push(num);

 arr.sort(function(a,b) {
  return a - b;
});
return arr.indexOf(num);
}

getIndexToIns([40, 60], 50);
```
<details>
  <p>First we need to insert the number into the array by using **.push()** to create one array. </p>
  <p>We use the **.sort()** which takes in a function and returns the lowest number. </p>
  <p>Once everything has been sorted, we use **.indexOf()** to check and return were the value should be </p>
</details>
