# Razor Pages

#### Razor Pages

*  A new aspect of ASP.NET Core MVC that makes coding page-focused scenarios easier and more productive.

#### Razor Pages vs MVC

* Razor Pages is recent and MVC is well established. 
* In Razor Pages request routing goes through the Pages folder. 
* Every Razor Page can have a corresponding Page Model. That model to have the same name as the corresponding Razor page but with a .cs appended.
* The view is in the Razor Page
* To display data in Razor pages properties need to be added to the Page Model.
* In Razor Pages everything lives in the Pages folder by default. Each Razor Page consists of the View template (.cshtml) and a corresponding .cs file which effectively acts as a controller action, specifically for that view.

#### Getting started with Razor Pages

**Create a Razor Pages Web App:**
* From the Visual Studio File menu, select New > Project.
* Create a new ASP.NET Core Web Application and select Next.
* Name the project RazorPagesMovie. It's important to name the project RazorPagesMovie so the namespaces will match when you copy and paste code.
* Select ASP.NET Core 2.2 in the dropdown, Web Application, and then select Create.

**Run the App**
* Press Ctrl+F5 to run without the debugger.

**Examine the Project Files**
* Pages folder: 
  contains Razor pages and supporting files. Each Razor page is a pair of files:
	* A .cshtml file that contains HTML markup with C# code using Razor syntax.
	* A .cshtml.cs file that contains C# code that handles page events.
  Supporting files have names that begin with an underscore.
* wwwroot folder: Contains static files, such as HTML files, JavaScript files, and CSS files
* appSettings.json: Contains configuration data, such as connection strings.
* Program.cs: Contains the entry point for the program.
* Startup.cs: Contains code that configures app behavior.