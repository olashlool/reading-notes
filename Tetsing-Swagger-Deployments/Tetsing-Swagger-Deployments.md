# Reading 17: Tetsing, Swagger, Deployments

## Swagger

- Swagger is a language-agnostic specification for describing REST APIs. The Swagger project was donated to the OpenAPI Initiative, where it's now referred to as OpenAPI. Both names are used interchangeably; however, OpenAPI is preferred. It allows both computers and humans to understand the capabilities of a service without any direct access to the implementation (source code, network access, documentation). One goal is to minimize the amount of work needed to connect disassociated services. Another goal is to reduce the amount of time needed to accurately document a service.

- The core to the OpenAPI flow is the specification—by default, a document named openapi.json. It's generated by the OpenAPI tool chain (or third-party implementations of it) based on your service. It describes the capabilities of your API and how to access it with HTTP. It drives the Swagger UI and is used by the tool chain to enable discovery and client code generation.

- Swagger UI offers a web-based UI that provides information about the service, using the generated OpenAPI specification. Both Swashbuckle and NSwag include an embedded version of Swagger UI, so that it can be hosted in your ASP.NET Core app using a middleware registration call.

## Unit Testing

- Imagine that we want to test whether or not the ProductController returns the right view. We want to make sure that when the ProductController.Details() action is invoked, the Details view is returned. The test class in Listing 2 contains a unit test for testing the view returned by the ProductController.Details() action.

- The class in Listing 2 includes a test method named TestDetailsView(). This method contains three lines of code. The first line of code creates a new instance of the ProductController class. The second line of code invokes the controller's Details() action method. Finally, the last line of code checks whether or not the view returned by the Details() action is the Details view.

- The ViewResult.ViewName property represents the name of the view returned by a controller. One big warning about testing this property. There are two ways that a controller can return a view.

        public ActionResult Details(int Id) { return View("Details"); }

- Alternatively, the name of the view can be inferred from the name of the controller action like this:

        public ActionResult Details(int Id) { return View(); }

- This controller action also returns a view named Details. However, the name of the view is inferred from the action name. If you want to test the view name, then you must explicitly return the view name from the controller action.

- An MVC controller passes data to a view by using something called View Data. For example, imagine that you want to display the details for a particular product when you invoke the ProductController Details() action. In that case, you can create an instance of a Product class (defined in your model) and pass the instance to the Details view by taking advantage of View Data.

- The modified ProductController in Listing 3 includes an updated Details() action that returns a Product

  > First, the Details() action creates a new instance of the Product class that represents a laptop computer. Next, the instance of the Product class is passed as the second parameter to the View() method.

- A more complex controller action might return different types of action results depending on the values of the parameters passed to the controller action. A controller action can return a variety of types of action results including a ViewResult, RedirectToRouteResult, or JsonResult.