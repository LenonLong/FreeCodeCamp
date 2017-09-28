#Title Case a sentence
## Return the provided string with the first letter of each word capitalized. Make sure the rest of the word is in lower case. For the purpose of this exercise, you should also capitalize connecting words like "the" and "of".

```javascript
function titleCase(str) {
var newStr = str.toLowerCase().split(' ').map(function(str) {
  return str.toUpperCase().charAt(0) + str.slice(1);
}).join(' ');


}
titleCase("I'm a little tea pot");
```

<details>
<p> First we have lowercase and split the str. </p>
<p>We then use the .map function which provides a callback for each of the words in the string. </p>
<p> As we iterate over every word, we use the **toUpperCase()** to capitalize the first letter in our string **.charAt(0)** and then end it by using the **slice()** method. </p>
<p> We then use the **join()** method to join it all back together. </p>
</details>
