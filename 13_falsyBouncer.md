##Falsy bouncer
<p>Remove all falsy values from an array </p>

```javascript
function bouncer(arr) {
  // use .filter() 
   return arr.filter(Boolean);
}

bouncer([7, "ate", "", false, 9]);
```

<details>
  <p>Any 0, -0, null, false, NaN, udefined, or empty string (" ") are considered a Boolean Value. </p>
  <p>By using the .filter() method we can pass in the Boolean syntax to filter any falsy elements</p>
</details>
