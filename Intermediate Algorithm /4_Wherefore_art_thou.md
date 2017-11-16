
## Wherefore art thou

<p>Make a function that looks through an array of objects (first argument) and returns an array of all objects that have matching property and value pairs (second argument). Each property and value pair of the source object has to be present in the object from the collection if it is to be included in the returned array.</p>

<p>For example, if the first argument is [{ first: "Romeo", last: "Montague" }, { first: "Mercutio", last: null }, { first: "Tybalt", last: "Capulet" }], and the second argument is { last: "Capulet" }, then you must return the third object from the array (the first argument), because it contains the property and its value, that was passed on as the second argument.</p>

```javascript
function whatIsInAName(collection, source){

  var sourceKey = Object.keys(source);

  return collection.filter(function(obj) {
    return sourceKey.every(function(key) {
      return obj.hasOwnProperty(key) && obj[key] === source[key];
    });
  });
}

whatIsInAName([{ first: "Romeo", last: "Montague" }, { first: "Mercutio", last: null }, { first: "Tybalt", last: "Capulet" }], { last: "Capulet" });

//  Answer: [{"first": "Tybalt", "last": "Capulet"}]

```

<details>
<p>First we need to extract the key, which would be {last: 'Capulet'}. We do this by using Object.keys(source)</p>
<p>We return the collection with .filter() and return sourceKey with .every() which will test every value in the array. </p>
<p>Last we check and return with .hasOwnProperty() and if any of the array objects contain {last: 'Capulet'}</p>
</details>
