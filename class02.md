
ES6 Classes
 Classes are a template for creating objects.

 Can a class declaration be hoisted?
  class declarations are not hoisted in the same way that function declarations are. Function declarations are hoisted to the top of their scope, meaning they can be invoked before their actual declaration in the code. However, class declarations are not fully hoisted and behave differently

 How would you describe a constructor and contextual “this” to a non-technical friend?
   A constructor is like a blueprint or a template for creating objects in JavaScript. It's a special function that is used to initialize and create new instances of an object with predefined properties and behaviors.

   "this" is a special keyword that refers to the current object instance. It allows us to access and modify the properties and methods of the object within its own scope.


Using Express Routing
 Within Express, what does routing refer to?
  routing refers to the process of determining how an application responds to a client request for a specific URL or route. Routing is responsible for mapping incoming requests to the corresponding handler functions that will generate the response
  
 What is the difference between a route path and a route method?
   route path and a route method are two distinct concepts that work together to define how an application handles incoming requests. Here's an explanation of the difference between the two: 
      Route Path:
        -The route path refers to the URL pattern or pattern matching expression that determines which requests are matched to a particular route.
        -It specifies the specific part of the URL that the server should consider when matching incoming requests.
        -Route paths can be simple strings, string patterns with named parameters, regular expressions, or a combination of these.
      Route Method:
        -The route method refers to the HTTP method or verb (such as GET, POST, PUT, DELETE) associated with a route.
        -It specifies the action or operation that the server should perform when a request matches a particular route.
        -Each route method is used to define a specific route for a particular HTTP method.

 When is it appropriate to add next as a parameter to a route handler and what must you do if next has been passed to your middleware as a parameter?      
  the next parameter is used to pass control to the next middleware function in the stack or to the next matching route handler. It is appropriate to add next as a parameter to a route handler when you want to explicitly pass control to the next middleware or route handler in the chain.
  If next has been passed to your middleware as a parameter, you need to ensure that you call next() when you want to pass control to the next middleware or route handler. If you don't call next(), the request-response cycle might not progress further, and subsequent middleware or route handlers won't be executed.
  Remember to call next() only when you want to pass control to the next middleware or route handler, as failing to do so can result in unexpected behavior or requests being left hanging without a response.


Express Routing
  What is an Express Router?
    Express Router is a feature that allows you to create modular, mountable sets of routes. It provides a way to organize and structure your application's routes into separate files or modules, making it easier to manage and maintain your codebase.

    Express Router acts as a mini Express application within your main Express application. It provides a routing system similar to the main Express application, allowing you to define routes, middleware, and handle requests. You can think of it as a smaller version of the main Express application dedicated to handling specific routes.
 
 By what mean do we initialize express.Router() in an express server?
   In an Express server, you initialize an Express Router by calling the express.Router() function. This function returns a new instance of an Express Router that you can use to define routes, middleware, and handle requests.

 What do we use route middleware for?
   Route middleware in Express is used to perform additional operations or logic specific to a particular route or group of routes. It allows you to intercept and modify the request and response objects, execute additional code, and control the flow of the request-handling process before reaching the final route handler.