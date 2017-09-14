# Check for Palindromes
## Return **true** if the given string is a palindrome. Otherwise, return **false**.

### A **palindrome** is a word or sentence that's spelled the same way both forward and backward, ignoring punctuation, case, and spacing

```javascript
function palindrome(str) {
  // check for regular expression / special characters
  var regularExpression = /[\W_]/g;
  // lowercase and replace
  var replaceStr = str.toLowerCase().replace(regularExpression, '');
  // split / reverse / join
  var newStr = replaceStr.split('').reverse().join('');

  // return with ternary operator / if newStr is equal to replaceStr, then true, else false
  return newStr === replaceStr ? true : false;

}
palindrome("eye");
```
