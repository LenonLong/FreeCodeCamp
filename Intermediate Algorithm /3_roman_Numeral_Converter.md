
##Roman Numeral Converter

```javascript

function convertToRoman(num) {
  var romans = {
    M: 1000,
    CM: 900,
    D: 500,
    CD: 400,
    C: 100,
    XC: 90,
    L: 50,
    XL: 40,
    X: 10,
    IX: 9,
    V: 5,
    IV: 4,
    I: 1
    };

    var result = '';

    for(var key in romans) {
      while(num >= romans[key]) {
        result += key;
        num -= romans[key]
      }
    }
    return result;
}

convertToRoman(36);
// XXXVI

```
<details>
<p>Convert the roman numeral to numbers. After, set your results to an empty string. </p>
<p>I used a for (var in ... loop) to find the the key value pairs. While the num passed in is greater than the numbers(value) of romans. The result of it will be the roman numeral. Whatever is left over is then subtracted by the number and we go through the loop again to find if the number is greater than. </p>
</details>
