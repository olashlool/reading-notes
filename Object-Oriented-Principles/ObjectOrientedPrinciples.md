# Object Oriented Principles

## Inheritance
- Inherited classes have all the same characteristics of the main class from which the original characteristics come from.
- Base class - The root class from which other classes can inherit their characteristics.
- Derived class - The class that has inherited characteristics and has the ability to extend/add upon them.
- A derived class implicitly inherits all the members of a base class except for its constructors and finalizers. It also reuses the base class' methods without having to reimplement them.
- Inheritance is transitive A derived class can have only one direct base class, but if ClassC is derived from ClassB, and ClassB is derived from ClassA, ClassC inherits the members declared in ClassB and ClassA.

## Abstract
###### The purpose of an abstract class is to provide a common definition of a base class that multiple derived classes can share.

- The abstract keyword allows for classes and class members to be incomplete, requiring them to be implemented in a derived class.
- Abstraction means hiding the unnecessary details from type consumers.

- The sealed keyword makes a class underivable, meaning it cannot be used as a base class.

## Polymorphism

> Polymorphism means that you can have multiple classes that can be used interchangeably, even though each class implements the same properties or methods in different ways.

> Polymorphism is often referred to as the third pillar of object-oriented programming, after encapsulation and inheritance. Polymorphism is a Greek word that means "many-shaped" and it has two distinct aspects

- At run time, objects of a derived class may be treated as objects of a base class in places such as method parameters and collections or arrays. When this polymorphism occurs, the object's declared type is no longer identical to its run-time type.

- Base classes may define and implement virtual methods, and derived classes can override them, which means they provide their own definition and implementation. At run-time, when client code calls the method, the CLR looks up the run-time type of the object, and invokes that override of the virtual method. In your source code you can call a method on a base class, and cause a derived class's version of the method to be executed.


## Object-Oriented programming (C#)
C# provides full support for object-oriented programming including abstraction, encapsulation, inheritance, and polymorphism.

1. Abstraction means hiding the unnecessary details from type consumers.
2. Encapsulation means that a group of related properties, methods, and other members are treated as a single unit or object.
3. Inheritance describes the ability to create new classes based on an existing class
4. Polymorphism means that you can have multiple classes that can be used interchangeably, even though each class implements the same properties or methods in different ways.