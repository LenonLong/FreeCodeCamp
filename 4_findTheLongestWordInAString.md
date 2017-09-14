#Find the longest word in a string
## Return the length of the longest word in the provided sentence. You should return a number.

```javascript
function findLongestWord(str) {
// we want to split the individual word by using .split()
var splitStr = str
// we need to store a total
var total = 0;
// loop through .length
for(var i = 0; i < splitStr.length; i++) {
  if(splitStr[i].length > total) {
    total = splitStr[i].length;
  }
}
return total;
}
findLongestWord("The quick brown fox jumped over the lazy dog");
```
