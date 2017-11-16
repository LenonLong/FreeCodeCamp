## Pig Latin

<p>Translate the provided string to pig latin.

Pig Latin takes the first consonant (or consonant cluster) of an English word, moves it to the end of the word and suffixes an "ay".

If a word begins with a vowel you just add "way" to the end.

Input strings are guaranteed to be English words in all lowercase. </p>

``` javascript

function translatePigLatin(str) {
  var firstVowel = str.search(/[aeiou]/);

    if(firstVowel > 0) {
      return str.slice(firstVowel) + str.slice(0, firstVowel) + 'ay';
    } else {
      return str + 'way'
    }
}

translatePigLatin("consonant");
// translatePigLatin("consonant") should return "onsonantcay"
// translatePigLatin("california") should return "aliforniacay".

```
<details>
<p>We first want to use .search() and pass in all of the vowels. </p>
<p>If we find a vowel, we want to cut and use the .slice() pass whatever has been cut to the back and add 'ay' at the end</p>
<p>If not, we just want to return the str and add 'way' at the end</p>
</details>
