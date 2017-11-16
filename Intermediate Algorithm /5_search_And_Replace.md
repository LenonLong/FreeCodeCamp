## Search and Replace

<p> Perform a search and replace on the sentence using the arguments provided and return the new sentence.
First argument is the sentence to perform the search and replace on.
Second argument is the word that you will be replacing (before).
Third argument is what you will be replacing the second argument with (after). </p>

<p>NOTE: Preserve the case of the original word when you are replacing it. For example if you mean to replace the word "Book" with the word "dog", it should be replaced as "Dog" </p>

```javascript

function myReplace(str, before, after) {

  if(before[0].toUpperCase() === before[0]){
    after = after[0].toUpperCase() + after.slice(1);
  }
  return str.replace(before, after);
}

myReplace("A quick brown fox jumped over the lazy dog", "jumped", "leaped");

// "A quick brown fox leaped over the lazy dog"
```
<details>
<p>If any before word that we want replace is case sensitive, we check and compare if the first letter of the before str is uppercased. </p>
<p>If it is, then the character of the after word str will become uppercased + we end anything afterwards with .slice() </p>
<p>Return with .replace()</p>
</details>
