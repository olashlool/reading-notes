# Classes & Memory Management

### What are Classes?
> A Class is like an object constructor, or a "blueprint" for creating objects.

### What is an Object?
> An object is a concrete entity based on a class, and is sometimes referred to as an instance of a class.

#### What is the difference between a class and an object?
> An Object is an instance of a class

## Create a Class
### To create a class, use the class keyword:

        class MyClass 
        {
            field ...
            methods ...
        }

## Create an Object
### An object is created from a class.

        MyClass myObj = new MyClass();

## Class inheritance
> it is possible to inherit fields and methods from one class to another. 
>> We group the "inheritance concept" into two categories:
>> - Derived Class (child) - the class that inherits from another class
>> - Base Class (parent) - the class being inherited from

#### To inherit from a class, use the : symbol.

        public class Child : Parent
        {
            fields...
            methods...
        }
### Constructors
> A constructor is a special method that is used to initialize objects. 
##### The advantage of a constructor: 
> 1. is that it is called when an object of a class is created. It can be used to set initial values for fields.
> 2. Constructors save time!

## NOTE: 
> - the constructor name must match the class name
> - it cannot have a return type
> - the constructor is called when the object is created.
> - All classes have constructors by default.

        public class Person
        {
            private string last;
            private string first;

        public Person(string lastName, string firstName)
        {
            last = lastName;
            first = firstName;
        }
            // Remaining implementation of Person class.
        }
## Properties
- A property is a member that provides a flexible mechanism to read, write or compute the value as a private fields
- Properties enable a class to expose a public away of getting and setting values while hiding the implementation or verification code
- a value keyword is used to define the value being assigned by the set or init accessor

## Stack and Heap
### What's the difference?
- Both are stored on computers RAM
- Stack memory keeps track of the order of how code is executed
- Heap memory keeps track of data and can be accessed in any order.
- Think of heap as boxes stacked on top of each other, we keep track of what's going on in our application by stacking another box on top when we call a method
- The Stack is like a stack of shoe boxes were we have to take off the top box to get to the one underneath
- The Stack is self maintaining meaning it takes care of its own memory management
- The Heap has to worry about Garbage collection

## Garbage Collection
- the GC (Garbage Collector) serves as an automatic memory manager
- It manages the allocation and release of memory for an application Benefits
- Frees Developers from having to manually release memory
- Allocates objects on the managed heap efficiently
- Reclaims objects that are no longer being used, clears their memory and keeps the memory available for future allocation
- Provides memory safety by making sure that an object cannot use the content of another object
- This is important so that your program does not use all the RAM of a computer and lower the performance of the computer's OS.
- C# provides automated garbage collection, but it is important to understand it in order to write the most efficient program.

