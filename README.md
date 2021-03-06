ASP.NET-MVC-Lambda-Expression-Helpers
=====================================
Extension methods allowing using Lambda Expressions instead of magic strings in your ASP.NET MVC 5 application. It resolves all route values, including areas and parameters in the method expression.

To install from NuGet:

	Install-Package System.Web.Mvc.Expressions
	
For other interesting packages check out:

 - [MyTested.AspNetCore.Mvc](https://github.com/ivaylokenov/MyTested.AspNetCore.Mvc) - fluent testing framework for ASP.NET Core MVC
 - [MyTested.WebApi](https://github.com/ivaylokenov/MyTested.WebApi) - fluent testing framework for ASP.NET Web API 2
 - [MyTested.HttpServer](https://github.com/ivaylokenov/MyTested.HttpServer) - fluent testing framework for remote HTTP servers
 - [AspNet.Mvc.TypedRouting](https://github.com/ivaylokenov/AspNet.Mvc.TypedRouting) - typed routing and link generation for ASP.NET MVC 6

Currently supported in Controller (add "using System.Web.Mvc.Expressions;"):

```
- RedirectToAction<HomeController>(c => c.Index())

- RedirectToActionPermanent<HomeController>(c => c.Index())

- AddModelError<FooInputModel>(m => m.Bar, "Invalid value for Bar.")

- AddModelError<FooInputModel>(m => m.Baz, new ArgumentException("Invalid value for Baz.")
```

Currently supported in Views (add namespace "System.Web.Mvc.Expressions" to the web.config file in the Views folder):
```
- Html.ActionLink<HomeController>(c => c.Index(5))

- Html.BeginForm<HomeController>(c => c.Index(5))

- Html.RenderAction<HomeController>(c => c.Index(5))

- Html.Action<HomeController>(c => c.Index(5))

- Url.Action<HomeController>(c => c.Index(5))

- Ajax.ActionLink<HomeController>(c => c.Index(5))

- Ajax.BeginForm<HomeController>(c => c.Index(5))
```
More info:
- Support for `ActionNameAttribute` which value overrides the action name when generating URL.

Contributors:

- Ivaylo Kenov
- Vladislav Karamfilov
