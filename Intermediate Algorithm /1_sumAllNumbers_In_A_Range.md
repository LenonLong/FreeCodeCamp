## Sum All Numbers In A range
<p> We'll pass you an array of two numbers. Return the sum of those two numbers and all numbers between them.  </p>
<p>The lower number will not always come first </p>

```javascript

function sumAll(arr) {
  var max = Math.max.apply(null, arr);
  var min = Math.min.apply(null, arr);
  var range = [];

  for(var i = min; i <= max; i++) {
    range.push(i);
  }
  return range.reduce(function(max, min) {
    return max + min;  
  });
}

sumAll([1, 4]);

Answer = 10
```

<details>
<p><strong>Step 1</strong>: We can't just use the <strong> Math.max(arr) </strong> because it will return NaN. Since we are passing the Array as an argument we use the Apply method to find the min & max numbers. </p>
<p><strong>Step 2</strong>: We create a loop where i is min and we see if it's less than the max. Then push.   </p>
<p><strong>Step 3</strong>: Return range and use the .reduce() method. It reduces a set of numbers to a single number and when you add it all up, you're left with the final result.</p>
</details>
