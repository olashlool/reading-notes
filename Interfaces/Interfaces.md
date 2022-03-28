# Interfaces
Inheritance describes the ability to reuse, extend and modify behavior defined in other classes by allowing any class to inherit the properties and methods of another.

Why do you need interfaces?

1. To achieve security - hide certain details and only show the important details of an object (interface).

2. C# does not support multiple inheritance

#### Interfaces vs Inheritance
- Review inheritance
    - no multiple inheritance
- Review Polymorphism
- Implementing an interface
    - naming conventions
    - properties
    - methods


### Notes :
- interfaces cannot be used to create objects.
- Interface methods do not have a body - the body is provided by the "implement" class
- On implementation of an interface, you must override all of its methods
- Interfaces can contain properties and methods, but not fields/variables
- Interface members are by default abstract and public
- An interface cannot contain a constructor (as it cannot be used to create objects)
