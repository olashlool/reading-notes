# View Components

### What Are View Components

* View components are similar to child actions and partials views, allowing you to create reusable components with (or without) logic. 

* View components include the same separation-of-concerns and testability benefits found between a controller and view. 
You can think of a view component as a mini-controller it's responsible for rendering a chunk rather than a whole 
response. 

* You can use view components to solve any problem that you feel is too complex with a partial.

### Writing A View Component

Like controllers, view components must be public, non-nested, and non-abstract classes that either:

* Derive from the ViewComponent class
* Are decorated with the [ViewComponent] attribute
* Have a name that ends with the "ViewComponent" suffix

### Rendering A View Component

* Within our Razor views, we can use the Component helper and its Invoke method to render view components. 
* The first argument (which is required) represents the name of the component.
* The remaining arguments (which are optional) represent parameters that our component's Invoke method might accept. 

### Returning Views from View Components

* The ViewComponent base class offers a View helper method for returning views. 

* That method looks for a Razor view in these two locations:
	* Views/Shared/Components/{ComponentName}/Default.cshtml
	* Views/{ControllerName}/Components/{ComponentName}/Default.cshtml

* If no explicit view name is specified, ASP.NET MVC 6 assumes the view to be named `Default.cshtml`. 

* That convention can be overridden by passing the view name as a string to the `viewName` parameter of the `View` method.

### Adding a View Model

* View model classes are defined as nested classes of the ViewComponent class.

### Asynchronous View Components

* View components can be asynchronous because the entire ASP.NET Core stack is asynchronous.

* Instead of an `Invoke` method, implement the `InvokeAsync` method and return a `Task<IViewComponentResult>`.

### Dependency Injection Within View Components

* ASP.NET Core has dependency injection built into the core of the stack. Therefore, we can have dependencies injected into the constructor of view components.