
##Diff Two Arrays
<p>Compare two arrays and return a new array with any items only found in one of the two given arrays, but not both. In others words, return the symmetric difference of the two arrays. </p>

``` javascript
function diffArray(arr1, arr2) {
  var newArr= arr1.concat(arr2);
  function filterArr(item) {
    if(arr1.indexOf(item) === -1 || arr2.indexOf(item) === -1){
      return item;
    }
  }
  return newArr.filter(filterArr);
}
diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);

// Answer = [4];

```

<details>
<p>We first want to concat arr1 to arr2.</p>
<p>I Created another function to check the indexOf both arr1 & arr1 </p>
<p>If there is no match, then return with .filter()</p>
</details>
