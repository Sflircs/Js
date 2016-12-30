# JavaScript Objects in Detail
---------------------------------

## How to Access Properties on an Object

The two primary ways of accessing properties of an object are with dot notation and bracket notation.

### 1. Dot Notation
```javascript
// We have been using dot notation so far in the examples above, here is another example again:​
​var book = {
  title: "Ways to Go", 
  pages: 280, 
  bookMark1:"Page 20"
};
​
​// To access the properties of the book object with dot notation, you do this:​
console.log ( book.title); // Ways to Go​
console.log ( book.pages); // 280
```

### 2. Bracket Notation
```javascript 
// To access the properties of the book object with bracket notation, you do this:​
console.log ( book["title"]); //Ways to Go​
console.log ( book["pages"]); // 280​
​
​//Or, in case you have the property name in a variable:​
​var bookTitle = "title";
console.log ( book[bookTitle]); // Ways to Go​
console.log (book["bookMark" + 1]); // Page 20 
```
Accessing a property on an object that does not exist will result in undefined.


## Accessing and Enumerating Properties on Objects
To access the enumerable (own and inherited) properties on objects, you use the for/in loop or a general for loop.
```javascript
// Create a new school object with 3 own properties: schoolName, schoolAccredited, and schoolLocation.​
​var school = {
  schoolName:"MIT", 
  schoolAccredited: true, 
  schoolLocation:"Massachusetts"
};
​
​//Use of the for/in loop to access the properties in the school object​
​for (var eachItem in school) {
  console.log(eachItem); // Prints schoolName, schoolAccredited, schoolLocation​
}
```


## Accessing Inherited Properties
Properties inherited from Object.prototype are not enumerable, so the for/in loop does not show them. However, inherited properties that are enumerable are revealed in the for/in loop iteration.
For example:
```javascript
//Use of the for/in loop to access the properties in the school object​
​for (var eachItem in school) {
  console.log(eachItem); // Prints schoolName, schoolAccredited, schoolLocation​
​
}

​// Create a new HigherLearning function that the school object will inherit from.​
​/* SIDE NOTE: As Wilson (an astute reader) correctly pointed out in the comments below, the educationLevel property is not actually inherited by objects that use the HigherLearning constructor; instead, the educationLevel property is created as a new property on each object that uses the HigherLearning constructor. The reason the property is not inherited is because we use of the "this" keyword to define the property.
*/​
​
​
​function HigherLearning () {
  this.educationLevel = "University";
}
​
​// Implement inheritance with the HigherLearning constructor​
​var school = new HigherLearning ();
    school.schoolName = "MIT";
    school.schoolAccredited = true;
    school.schoolLocation = "Massachusetts";
​
​//Use of the for/in loop to access the properties in the school object​
​for (var eachItem in school) {
  console.log(eachItem); // Prints educationLevel, schoolName, schoolAccredited, and schoolLocation​
}
```
In the last example, note the educationLevel property that was defined on the HigherLearning function is listed as one of the school’s properties, even though educationLevel is not an own property—it was inherited.




