##Seek and destroyer

<p>
You will be provided with an initial array (the first argument in the destroyer function), followed by one or more arguments. Remove all elements from the initial array that are of the same value as these arguments.
</p>

```javascript
function destroyer(arr) {
  var args = Array.from(arguments);

  function filteredArr(item) {
    return args.indexOf(item) === -1 ;
  }
  return arr.filter(filteredArr);
}
destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```

<details>
  <p> The **arguemnts object** is similar to an array, but does not have any array properties apart from length. That's why we need to convert the arguments into an array like object by using the **Array.from(arguents)** method. </p>
  <p>I created another function to compare and check args with **.indexOf()**</p>
  <p>Then use the **.filter()** to filter out the elements that are on the array and keep the ones that are not </p>
</details>
