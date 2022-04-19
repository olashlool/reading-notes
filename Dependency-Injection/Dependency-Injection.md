# Reading 13: Dependency Injection

## Dependency Injection

- Dependency injection (DI) software design pattern, is a technique for achieving Inversion of Control (IoC) between classes and their dependencies.

- A dependency is any object that another object requires. Code dependencies are problematic and should be avoided.

- Dependency injection addresses dependency problems through:

  - The use of an interface or base class to abstract the dependency implementation.
  - Registration of the dependency in a service container. ASP.NET Core provides a built-in service container, IServiceProvider. Services are registered in the app's Startup.ConfigureServices method.
  - Injection of the service into the constructor of the class where it's used. The framework takes on the responsibility of creating an instance of the dependency and disposing of it when it's no longer needed.

## The Repository Design Pattern

- Repositories are classes or components that encapsulate the logic required to access data sources.

- Repositories centralize common data access functionality, providing better maintainability and decoupling the infrastructure or technology used to access databases from the domain model layer.

- In an Object-Relational Mapper (ORM) like Entity Framework, the code that must be implemented is simplified, thanks to LINQ and strong typing. This lets you focus on the data persistence logic rather than on data access plumbing.

- The repository design pattern has two purposes:

  1. An abstraction of the data layer. The methods are based on the CRUD methods; Create, Read, Update and Delete.
  2. A way of centralizing the handling of the domain objects.

## SOLID Principles

- The SOLID principles of software development are five principles that software developers could use to guide them in creating software that was well designed, high quality and easy to maintain:

  1. #### Single Responsibility Principle (SRP)

     Every class or method in your application should have exactly one (a single) job or responsibility and only one reason to change. By ensuring that we are writing methods and classes that have only one responsibility, we make these methods easier to test. Methods that try to do too much tend to require tests with more complex and elaborate “Arrange” sections that make the test longer and more difficult to understand and maintain.

  2. #### The Open/Close Principle (OCP)

     OCP states that software, be it a method or a class, should be open for extension, but closed to modification. OCP is a concept that unifies two tenants of OOP: Encapsulation and Inheritance.

  3. #### The Liskov Substitution Principle (LSP)

     An object in your application should be able to be replaced with a type derived from it without breaking the application. According to LSP, if my application is expecting an object of type “Animal” I should be able to pass in any class derived from Animal (Dog, Cat, Fish, etc.) without there being any problem or issue.

  4. #### The Interface Segregation Principle (ISP)

     Clients should not be forced to rely on interfaces they do not use. You should make fine grained interfaces that are specific to the functions and needs of the client. Dealing with a smaller and more targeted interface makes developing against that service much easier. And since a class can implement as many interfaces as you need it to, there’s really not any technological barrier to keeping these interfaces finely grained.

  5. #### The Dependency Inversion Principle (DIP)

     Code should depend on abstractions; not concrete implementations. Furthermore, those abstractions should not depend on the details; the details should depend on the abstractions.

- Dependency Inversion is not the same thing as Dependency Injection. Dependency Injection is a methodology of achieving Dependency Inversion, but they are not the same thing.
