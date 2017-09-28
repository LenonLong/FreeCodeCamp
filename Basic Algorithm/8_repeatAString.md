##Repeat a given string (first argument) num times (second argument). Return an empty string if num is not a positive number.

```javascript
function repeatStringNumTimes(str, num) {
  var newStr = '';
  while(num > 0) {
    newStr += str;
    num --;
  }
  return newStr;
}
repeatStringNumTimes("abc", 3);
```
