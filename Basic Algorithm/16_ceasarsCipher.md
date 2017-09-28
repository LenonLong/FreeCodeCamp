##Ceasars cipher

<p>One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. In a shift cipher the meanings of the letters are shifted by some set amount.

A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus 'A' ↔ 'N', 'B' ↔ 'O' and so on.

Write a function which takes a ROT13 encoded string as input and returns a decoded string.

All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on. </p>

```javascript
function rot13(str) {
//
var newStr = str.split('').map(cipher).join('');
return newStr;
}
function cipher(letter) {
    var symbolregex = /[^a-zA-Z]/g;
    // test the regular expression
      if(symbolregex.test(letter)) {
        return letter;
      }
        // the ranges for A - Z is 65 - 90
      var codeAskii = letter.charCodeAt(0);
    // if the start of the code letter is greater than 77
      if(codeAskii > 77) {
    // we want to - 13
        codeAskii -= 13;
      } else {
    // less than 77 + 13
        codeAskii += 13;
      }
    return  String.fromCharCode(codeAskii);
 }

console.log(
  rot13("SERR PBQR PNZC")
  // FREE CODE CAMP
);
```

<details>
  <p> We first want to use the **.split('')** method to manipulate the string to an array, then use the  **.map()** to go through the whole array, then **.join()** the array together so it becomes a string.</p>
  <p> We check and test for regular expression by using the
  -- var symbolregex = /[^a-zA-Z]/g; -- </p>
  <p>In our if statement we used the **.test(letter)** to test the string to see if any regular expression matches. Were basically testing if it's going to come back as a Boolean. </p>

  <p>**.charCodeAt** returns a number for each letter. For example 65 = A , and 90 = Z. But remember we only want the capital letters of A - Z.. So we only stick to 65 - 95! </p>
  <p>Since our code shift by 13 all we have to do is +13 & -13. We accomplish this by utilizing an if statement, then returning **String.fromCharCode** which will return a string created by a sequence of unicode values. </p>

  <p>After a long process of trying to solve this, our rot13 will = FREE CODE CAMP. </p>
</details>
