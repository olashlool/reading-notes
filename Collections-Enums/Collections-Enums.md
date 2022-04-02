# Collections AND Enums

### Collections 

> Collections are a flexible way to work with groups of objects. Unlike arrays, the group of objects you work with can grow and shrink dynamically as the needs of the application change. For some collections, you can assign a key to any object that you put into the collection so that you can quickly retrieve the object by using the key. A collection is a class, so you must declare an instance of the class before you can add elements to that collection.

##### NOTE:
- Foreach loops cannot be used in normal collections, but a regular for loop can.
- System.Collections classes do not store elements are specific types but instead as type Objects. These are legacy types and should be avoided whenever possible, but some examples include ArrayList, Hashtable, Queue, and Stack.

##### Enumeration types
- Enumeration types are "value types defined by a set of named constants of the underlying integral numeric type." The default values are of type int if not specified, starting at 0 and increasing.
- System.Enum is the abstract base class of all enumeration types, providing methods to get info about the enumeration type and its values.
- For any enum type, there are explicit conversions between enum type and underlying integral typecasting an enum value to its underlying type will result in the associated integral value being given.