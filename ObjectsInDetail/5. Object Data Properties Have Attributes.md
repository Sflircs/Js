# JavaScript Objects in Detail
---------------------------------

## Object Data Properties Have Attributes
Each data property (object property that store data) has not only the name-value pair, but also 3 attributes (the three attributes are set to true by default):

— **Configurable Attribute:** Specifies whether the property can be deleted or changed.

— **Enumerable:** Specifies whether the property can be returned in a for/in loop.

— **Writable:** Specifies whether the property can be changed.

Note that ECMAScript 5 specifies accessor properties along with the data properties noted above. 
And the accessor properties are functions (getters and setters).
