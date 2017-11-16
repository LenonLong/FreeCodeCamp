## DNA Pairing

<p>The DNA strand is missing the pairing element. Take each character, get its pair, and return the results as a 2d array.

Base pairs are a pair of AT and CG. Match the missing element to the provided character.

Return the provided character as the first element in each array.

For example, for the input GCG, return [["G", "C"], ["C","G"],["G", "C"]]

The character and its pair are paired up in an array, and all the arrays are grouped into one encapsulating array</p>

```javascript

function pairElement(str) {
  var pairs = {A: 'T', T: 'A', C: 'G', G: 'C'};

  str.split('').map(function(key) {
    return [key, pairs[key]];
  });
}
pairElement("GCG");
// pairElement("GCG") should return (["G", "C"], ["C", "G"], ["G", "C"])

// pairElement("ATCGA") should return [["A","T"],["T","A"],["C","G"],["G","C"],["A","T"]]
```
<details>
<p>Since we already know the base pairs of DNA that was given to us all we want to do afterwards
is split the string then map through the objects. </p>
<p>We return the key with the key value pairs</p>
</details>
