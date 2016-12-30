

First, every JavaScript function has a **prototype property** (this property is empty by default), and you attach properties and methods on this prototype property when you want to implement inheritance. 
This prototype property is not enumerable; that is, it isn’t accessible in a for/in loop. 
But Firefox and most versions of Safari and Chrome have a **\_\_proto\_\_** “pseudo” property (an alternative syntax) that allows you to access an object’s prototype property. 

You will likely never use this **\_\_proto\_\_** pseudo property, 
but you should know that it exists and it is simply a way to access an object’s prototype property in some browsers.
The prototype property is used primarily for inheritance; you add methods and properties on a function’s prototype property to make those methods and properties available to instances of that function.

Consider this simple example of inheritance with the prototype property (more on inheritance later):
```javascript
function PrintStuff (myDocuments) {
​this.documents = myDocuments;
}
​
​// We add the print () method to PrintStuff prototype property so that other instances (objects) can inherit it:​
PrintStuff.prototype.print = function () {
console.log(this.documents);
}
​
​// Create a new object with the PrintStuff () constructor, 
// thus allowing this new object to inherit PrintStuff's properties and methods.​
​var newObj = new PrintStuff ("I am a new Object and I can print.");
​
​// newObj inherited all the properties and methods, including the print method, from the PrintStuff function. 
// Now newObj can call print directly, even though we never created a print () method on it.​
newObj.print (); //I am a new Object and I can print.

```
