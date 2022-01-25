# Razor ASP.NET

Razor is an ASP.NET programming syntax used to create dynamic web pages with the C# or VB.NET programming languages. Razor was in development in June 2010[3] and was released for Microsoft Visual Studio 2010 in January 2011.[4] Razor is a simple-syntax view engine and was released as part of MVC 3 and the WebMatrix tool set.[4]

Razor became a component of AspNetWebStack and then became a part of ASP.NET Core.

 

[](#c-tools)C# tools
====================

[](#general)General
-------------------

*   [Mediator](https://github.com/jbogard/MediatR) - Simple CQS library
*   [Polly](https://github.com/App-vNext/Polly) - Provides exception handling policies such as Retry, Wait and Retry or Circuit Breaker.
*   [Refit](https://github.com/reactiveui/refit) - Create strongly typed, injectable interfaces for APIs.
*   [Swashbuckle](https://docs.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-swashbuckle?view=aspnetcore-3.1&tabs=visual-studio) - A wrapper to auto-generate and serve a Swagger document for an application's endpoints.

[](#validation)Validation
-------------------------

*   [Fluent Validation](https://fluentvalidation.net/) - Fluent validation rules which can be applied as middleware.

[](#messaging)Messaging
-----------------------

*   [Mass transit](https://masstransit-project.com/) - A high-level abstraction over messaging buses such as Azure Service Bus and RabbitMQ. Provides a class/interface implementation of exchanges.

[](#testing)Testing
-------------------

*   [Simmy](https://github.com/Polly-Contrib/Simmy) - Chaos engineering library used for testing intermittent errors and exceptions.
*   [Moq](https://github.com/Moq/moq4/wiki/Quickstart) - Strongly typed mocking & stubbing library.

[](#vue-tools)Vue tools
-----------------------

*   [Vuex](https://vuex.vuejs.org/) - State management store for Vue applications.
*   [Nuxt](https://nuxtjs.org/) - A high-level framework providing features such as server-side rendering and static site generation.

[](#architecture-resilience-patterns)Architecture resilience patterns
=====================================================================

*   [Bulkhead](https://docs.microsoft.com/en-us/azure/architecture/patterns/bulkhead)
*   [Circuit breaker](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/implement-resilient-applications/implement-circuit-breaker-pattern)