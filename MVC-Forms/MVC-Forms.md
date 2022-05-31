# Reading 27: MVC Forms

## View Models

Views are how the server renders a "front-end" user interface. They are a combination of HTML and C# code, 
written with Razor Syntax. Views have a .cshtml file extension.

#### Benefits of Views

- App is easier to maintain due to better organization.
- Parts are loosely coupled.
- Easier to test user interface parts.
- Due to organization, repeat sections are unlikely.

#### How controllers specify views

- Views from actions are returned as a ViewResult(a type of ActionResult).

- Since most controllers inherit from Controller, simply use the View() helper method to return ViewResult().

- View method has several overloads

    1. An explicit view to return

            return View("Orders");
    2. A model to pass to the view

            return View(Orders);

    3. Both a view and a model
    
            return View(Order, "Orders");

    4. When an action returns a view, view discovery takes place. By default "return View();" will return a view with the same name as the action method from which it's called. For example

            return View(About)
    5. Will search for a view file named About.cshtml. A view path can be provided instead of a view name

            return View("Views/Home/About.cshtml")

#### Differences between ViewData and ViewBag

ViewData is a dictionary of objects that is derived from ViewDataDictionary class and accessible using strings as keys. 
ViewBag is a dynamic property that takes advantage of the new dynamic features in Csharp 4.0. Internally ViewBag properties 
are stored as name, value pairs in the ViewData dictionary.

## 4 Ways To Create Form In ASP.NET MVC

- Forms Weakly Typed (Synchronous)
- Forms Strongly Typed (Synchronous)
- Forms Strongly Typed AJAX (Asynchronous)
- Forms HTML, AJAX and JQUERY

#### Forms - Weakly Typed
Advantage

- It’s easy to create a form using Weakly Typed Mechanism.
- Mostly used when you ned to create a form with one or two input items.

Disadvantage

- Because it is not strongly typed, IntelliSense doesn’t help you.
- Have a higher chance of getting exception and runtime error messages.
- Very difficult to manage when forms have multiple input items and controls.
- It is very clumsy when you need to add or remove input items.
