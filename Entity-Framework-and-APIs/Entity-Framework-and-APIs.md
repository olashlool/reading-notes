# Reading 12: Entity Framework and APIs

## ASP.NET MVC web app

The ASP.NET Core MVC framework is a lightweight, open source, highly testable presentation framework optimized for use with ASP.NET Core.

ASP.NET Core MVC provides a patterns-based way to build dynamic websites that enables a clean separation of concerns. It gives you full control over markup, supports TDD-friendly development and uses the latest web standards.

ASP.NET Core MVC includes the following:

- Routing
- Model binding
- Model validation
- Dependency injection
- Filters
- Areas
- Web APIs
- Testability
- Razor view engine
- Strongly typed views
- Tag helpers
- View Components

## Entity Framework Core

Entity Framework (EF) Core is a lightweight, extensible, open source and cross-platform version of the popular Entity Framework data access technology

EF Core can serve as an object-relational mapper (O/RM), enabling .NET developers to work with a database using .NET objects, and eliminating the need for most of the data-access code they usually need to write.

EF Core supports many database engines.

### The Model

With EF Core, data access is performed using a model. A model is made up of entity classes and a context object that represents a session with the database, allowing you to query and save data. You can generate a model from an existing database, hand code a model to match your database, or use EF Migrations to create a database from your model, and then evolve it as your model changes over time.

### Querying

Instances of your entity classes are retrieved from the database using Language Integrated Query (LINQ).

### Saving Data

Data is created, deleted, and modified in the database using instances of your entity classes.

## Data Seeding

- Data seeding is the process of populating a database with an initial set of data.

- There are several ways this can be accomplished in EF Core:

  - ### Model seed data

    Seeding data can be associated with an entity type as part of the model configuration. Then EF Core migrations can automatically compute what insert, update or delete operations need to be applied when upgrading the database to a new version of the model.

  - ### Manual migration customization

    When a migration is added the changes to the data specified with HasData are transformed to calls to InsertData(), UpdateData(), and DeleteData(). One way of working around some of the limitations of HasData is to manually add these calls or custom operations to the migration instead.

  - ### Custom initialization logic

    A straightforward and powerful way to perform data seeding is to use DbContext.SaveChanges() before the main application logic begins execution.

- The seeding code should not be part of the normal app execution as this can cause concurrency issues when multiple instances are running and would also require the app having permission to modify the database schema.

## Razor Pages

Razor Pages is an aspect of ASP.NET Core MVC that makes coding page-focused scenarios easier and more productive.

## Youtube: Building Web APIs with ASP.NET Core 2.0

What is a Web API?

- An HTTP service
- Logic or data accessible

HTTP refresher

- Application layer protocol
- Used to access resources identified by a URI
- Access resources using standardized methods/verbs
- Stateless request-reply protocol
- Headers and response bodies - formats
- Status codes indicate the type of response

Status codes:

- 200 level: a good request
- 400 client side problem
- 500 internal service error

Handling HTTP requests with ASP.NET Core

- The server (kestrel) listens for requests
- The middleware pipeline is invoked for each request
- Use MVC to route requests to a controller and action
- Responses flows back down the middleware pipeline

To create a Web API

- Create an ASP.NET Core project
- Setup MVC
- Create a class that derives from ControllerBase
- Implement your Action Methods

Route templates

- Extract route values (ex "api/orders/{id}")
- Use route tokens (ex "api/[controller]")
- Optional route values: {id?}
- Default route values

Model binding and validation

- Bind request data to action parameters
- Bind form data, route values and query string parameters by default
- Use [FromBody] to bind the reqeust body using formatters User [FromRoute/Query/Form/Header] to restrict model binding to a particular source
- Use data annotations and check ModelState.IsValid

## User Secrets

What are they?

> A secure way of storing private user information such as API keys, clients secrets,and connection strings. Anything you don't want others to know about when using code base. You will be able to access user secrets with controllers.
