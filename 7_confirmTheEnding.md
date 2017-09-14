##Confirm the ending
###Check if a string (first argument, str) ends with the given target string (second argument, target).
### we can't use the .endsWith()

```javascript
function confirmEnding(str, target) {
  // we target the the string by using the substr() method and use -target to target the end of the string
  var checkStr = str.substr(-target.length);
  return checkStr === target ? true : false;

}
confirmEnding("Bastian", "n");
```
