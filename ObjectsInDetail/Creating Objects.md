# JavaScript Objects in Detail
--------------------------------
**Objects can contain any other data type, including Numbers, Arrays, and even other Objects.**

These are the two common ways to create objects: 
### 1. Object Literals
The most common and, indeed, the easiest way to create objects is with the object literal described here:
```javascript
// This is an empty object initialized using the object literal notation​
​var myBooks = {};
​
​// This is an object with 4 items, again using object literal​
​var mango = {
  color: "yellow",
  shape: "round",
  sweetness: 8,
​
​howSweetAmI: function () {
    console.log("Hmm Hmm Good");
  }
}
```


### 2. Object Constructor
The second most common way to create objects is with Object constructor. 
A constructor is a function used for initializing new objects, and you use the new keyword to call the constructor.
```javascript
var mango =  new Object ();
    mango.color = "yellow";
    mango.shape= "round";
    mango.sweetness = 8;
​
mango.howSweetAmI = function () {
  console.log("Hmm Hmm Good");
}
```
