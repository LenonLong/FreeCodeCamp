##Truncate a string (first argument) if it is longer than the given maximum string length (second argument).
###Return the truncated string with a '...' ending. Note that inserting the three dots to the end will add to the string length. However, if the given maximum string length num is less than or equal to 3, then the addition of the three dots does not add to the string length in determining the truncated string.

```javascript
function truncateString(str, num) {
  if(str.length > num && num >= 3) {
    return str.splice(0, num-3) + '...';
  } else if (str.length > num && num <= 3) {
    return str.splice(0, num);
  } else {
    return str + '...';
  }
}

truncateString("A-tisket a-tasket A green and yellow basket", 11);
```

<details>
  <p>For this algo challenge I knew that if the lenght of the string and if the number given was greater than, I had to subtract 3 from the num in the str.splice to compensate for the three '...' added to the end of the string  </p>
  <p>I'm sure I could've use the trim() method to take away the white spaces but i'll save that for another challenge!  </p>
</details>
