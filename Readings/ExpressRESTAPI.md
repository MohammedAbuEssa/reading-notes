# Express REST API

**Classes are a template for creating objects.**

**Can a class declaration be hoisted?**
In JavaScript, class declarations are not hoisted.

**How would you describe a constructor and contextual “this” to a non-technical friend?**
In simple words, a constructor is a way to create more than one item with the same proprites without the need to redeclare the proprites.
and you can create an object from the constructor by just calling the constructor and passing the properties; "this" is a way to let the constructor know that this object has this property.

**Within Express, what does routing refer to?**
Refers to how an application’s endpoints (URIs) respond to client requests. For an introduction to routing

**What is the difference between a route path and a route method?**
A route method is derived from one of the HTTP methods, and is attached to an instance of the express class.

Route paths, in combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.

**When is it appropriate to add next as a parameter to a route handler and what must you do if next has been passed to your middleware as a parameter?**

The "next" parameter is used in middleware functions to pass control to the "next" middleware or route handler. If "next" is passed to your middleware, simply call it to proceed to the "next" function in the chain. This allows subsequent functions to handle the request accordingly.

**What is an Express Router?**
It is a mini express application without all the bells and whistles of an express application, just the routing stuff.

**By what mean do we initialize express.Router() in an express server?**
We will call an instance of the express.Router(), apply routes to it, and then tell our application to use those routes.

**What do we use route middleware for?**
Route middleware in Express is a way to do something before a request is processed.
