## Mutations
<p> Return true if the string in the first element of the array contains all of the letters of the string in the second element of the array.

For example, ["hello", "Hello"], should return true because all of the letters in the second string are present in the first, ignoring case.

The arguments ["hello", "hey"] should return false because the string "hello" does not contain a "y".

Lastly, ["Alien", "line"], should return true because all of the letters in "line" are present in "Alien".</p>

```javascript
function mutation(arr) {
  var firstArr = arr[0].toLowerCase();
  var secondArr = arr[1].toLowerCase();

  for(var i = 0 ; i < secondArr.length; i++) {
    // check by using .indexOf()  / if found return false.
    if(firstArr.indexOf(secondArr[i]) === -1) {
      return false;
    }
  }
    return true;
}
mutation(["voodoo", "no"]);
```

<details>
 <p>I create two separate var to compare to one another and used the **.toLowerCase()** </p>
 <p>Since I wanted to compare the secondArr to the first, I used the **.indexOf()** which will check the firstArr if it has any elements present to the secondArr. </p>
 <p> -1 will always return false, else return true </p>
</details>
