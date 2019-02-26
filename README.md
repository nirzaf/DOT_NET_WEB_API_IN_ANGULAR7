# JWT Authentication with .Net Core Web API and Angular 7



# Before Running this Project

Install npm packages using 'npm install' command from Angular 7 folder.

How ASP.NET Core 1.0 Middleware is different from HttpModule
 March 9, 2016  Talking Dotnet  ASP.NET, ASP.NET Core
Earlier I posted about changes in ASP.NET Core 1.0 and one of the biggest change is in HTTP pipeline. We as ASP.NET developers are quite familiar with HttpHandler and HttpModules but with this new version of ASP.NET, they are gone. They are replaced with a new better, cleaner and easy to implement approach called “Middleware“. You can think of Middleware is a combination of HttpHandler and HttpModule. In this post, find out how ASP.NET Core 1.0 Middleware is different from HttpModule.

Before we move to similarities and differences, let’s talk briefly about HttpHandler, HttpModules and Middleware.

HttpHandler
HttpHandler are extension based. They used to handle requests for file name with specific extension, such as .rss. The most common handler is an ASP.NET page handler that processes .aspx files. When users request an .aspx file, the request is processed by the page through the page handler. You can configure them in web.config.

HttpModule
HttpModules are event based. It is called on every request that is made to your application. HTTP modules are called as part of the ASP.NET request pipeline and have access to life-cycle events throughout the request. And they are also configured via web.config or Global.asax.

Middleware
The definition provided by OWIN specification for MiddleWare is closest, in relation to ASP.NET Core 1.0.

Middleware – Pass through components that form a pipeline between a server and application to inspect, route, or modify request and response messages for a specific purpose.

You can think of Middleware as small application components that can be incorporated into an HTTP request pipeline. It is a combination of both HTTP modules and handlers that we’ve had in classic ASP.NET. You can use Middleware to implement various tasks when processing requests such as authentication, session state retrieval and persistence, logging and so on.

Similarity between Middleware and HttpModule
Middlewares are similar to HttpModules as they serve the same purpose. Like modules, middlewares are also executed in every single request, both needs to be configured and can be used to generate their own HTTP response.
 
