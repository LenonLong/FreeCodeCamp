##Slasher flick
<p> Return the remaining elements of an array after chopping off n elements from the head.
The head means the beginning of the array, or the zeroth index.</p>

```javascript
function slasher(arr, howMany) {
  // using .splice() will destroy/remove from index 2 and anything after that.
  return arr.splice(howMany);
}
slasher([1, 2, 3], 2);
```
