# Reading 26: Intro to MVC

## Azure Dev Ops

Azure DevOps is a service that allows teams to organize, plan, and work on code development in a single location. Azure DevOps has integrated features that work with IDEs such as:

- Azure Repos: provides Git repositories for version control.
- Azure Pipelines: provides build and release services for application delivery and integration.
- Azure Boards: delivers a suite of Agile tools to help planning and tracking using Kanban and Scrum methods.
- Azure Test Plans: provides tools to test apps.
- Azure Artifacts: allows teams to share Maven, npm, and NuGet packages from public and private sources and integrate package sharing into your CI/CD pipelines.

## MVC Basics

MVC is a design pattern/architecture. It is desigend for efficiency.

- In MVC the View only deals with the UI and user actions are defined in Controller.
- MVC is action based architecture, which helps keep code clean and organized. Based on an action, a certain view is displayed.
- In MVC, we don't have View State to store the state information.
- In MVC action logic and UI are loosely coupled. Because of these they can be tested easily.

### Model
Layer represent the objects of the application.

### View
Layer contains all HTML controls to define UI. We can use Razor engine to help render View.

### Controller
Handles all requests from users. It's the engine of the MVC application.

The Controller is just a class wit ha group of methods called actions. Every action method returns a View.

**MVC is not a new framework: it is built on top of ASP.NET, so all the features available in ASP.NET are still availabe using MVC.**

## Tag Helpers
Tag helpers enable server side code to participate in creating and rendering HTML elements in a Razor file. Lets look at an example

    {
        public int ID { get; set; }
        public string Title { get; set; }
        public DateTime ReleaseDate { get; set; }
        public string Genre { get; set; }
        public decimal Price { get; set; }
    }

This code snippet would have a Razor markup that looks like

    <label asp-for="Movie.Title"></label>

In HTML this looks like:

    <label for="Movie_Title">Title</label>

## Bootstrap
- Acts as a toolkit for making front end views.
- Responsive in nature, based on a grid system.
- Defaults to 12 columns in the grid, but fully customizable.

    ### Columns
    - Can be set automatically class="col", or can be a width (out of 12) class="col-6".
    - Breakpoints are set using a few preset widths: class="col-sm" or class="col-lg" for example.
    - Breakpoints can be combined with column widths to adjust their style based on the breakpoint it is in: class="col-sm-9".
    - Offsets can be added for a specific column: class="col-sm offset-sm-3".

    ### Nav Bars
    - Start with **nav tag** with the class "navbar". In the nav section there needs to be an unordered list of class c"navbar-nav".
    - The list items themselves need classes of "navbar-item" and the links themselves need the class "nav-link".
    - The whole unordered list can but put in a div with the class "collapse navbar-collapse".
    - To allow the toggling of the collapsible navbar, add a button with the properties: class="navbar-toggler" data-toggle="collapse" data-target="{target id here}".
    - To make expand fully on a larger screen, the nav tag can have "navbar-expand-lg" added to its class. Adding "fixed-top" to it will make it stay at the top of the screen the whole time.

    ### Modals
    - Modals are the pop-up boxes that seem to darken the background and allow forms or text boxes to be interacted with.
    - To launch a modal, a button with class "btn btn-primary" and data-toggle="{modal id}".
    - The modal itself is a div with class "modal" that contains a div with class "modal-dialog" that then contains a div with class "modal-content".
    - For subsequent information in the modal, there are the tags: modal-header, modal-title, modal-body, modal-footer.
    - To add an exit button in the corner, make a button with class "close" and data-dismiss="modal".

    ### Forms
    - On a basic form with text boxes and a submit button, add the class "btn btn-primary".
    - For each label and entry field, they can be grouped in a div with class "form-group row" to link them together and organize them in a row.
    - The labels can have column classes to make their location change at different breakpoints for different screen sizes.

    ### List Groups
    - Start with a div with class "list-group".
    - Inside will be links with the class "list-group-item list-group-item-action".
    - To make these divs have "pills" with numbers next to them, create a span inside the link tags with class "badge badge-primary badge-pill".
    - These don't need to be links. They can be made into a list to act as a sort of feed. There are multiple uses with List Groups.

    ### Cards
    - Start with a div with class "card" and inside it have a div with class "card-body".
    - Inside the body there can be the "card-title", "card-text".
    - Above the body, if you want to add an image, use "card-img-top".
    - List groups also work very well inside of cards.

    ### Tables
    - Using an HTML table, add the class "table".
    - Other class additions are more self explanatory: "table-hover", "thead-dark", "table-dark", "table-striped", "table-bordered"

    ### Alerts
    - Create a div with class "alert". Feel free to add "alert-info" as well for color.
    - Inside a button with class "close" and data-dismiss of "alert" will allow it to be closed/removed.

    ### Navigation Options
    - Addition options for navigation bars include using "nav-pills", "nav-fill", "nav-tabs".
    - There are a slew of nav item options that are not as common but still available that can be found in the documentation.

