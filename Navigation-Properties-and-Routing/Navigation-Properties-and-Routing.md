# Reading 14: Navigation Properties and Routing

## Routing Within MVC

The ASP.NET routing module handles all incoming browsers requests and connects them to the appropriate controller actions.

### When starting an MVC application, a few things happen:

1. The Application_Start() method is called
2. The above method then calls the RegisterRoutes() method.
3. The RegisterRoutes() method then creates the route table.

The route table comes configured with a default route. This route contains:

- The controller name
- The controller action
- The parameter

Example: Route: /Home/Hotel/4

Home -> controller name Hotel -> controller action 4 -> parameter

## Routing within Core

Apps can configure routing using

- Controllers
- Razor Pages
- SignlarR
- gRPC Services
- Endpoint-enabled middleware such as Health Checks
- Delegates and lambdas registered with routing.

### Routing uses a pair of middleware

- UseRouting: adds route matching in the middleware pipeline.
- UseEndpoints: adds endpoint execution to the middleware pipeline.

MapGet method is used to define an endpoint.

### Endpoint definition

- Executable: Has a RequestDelegate
- Extensible: Has a metadata collection.
- Selectable: Optionally, has routing information.
- Enumerable: The collection of nedpoints can be listed by retrieving the EndpointDataSource from DI.
