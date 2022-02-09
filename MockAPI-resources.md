## mockAPI

https://mockapi.io/  

MockAPI is a simple tool that lets you easily mock up APIs, generate custom data, and preform operations on it using RESTful interface

Mocki: Mock API - Create and Simulate APIs for Testinghttps://mocki.io
Create, run and deploy mock APIs in minutes. Use your mock API to run tests independent of external services, design APIs and remove backend dependencies ...

Mockoon GUI cheat sheet



A quick and dirty API framework, mockapi is best suited for rapidly building API prototypes or mock APIs. It's built on express, but its specifically tailored for building REST APIs that return JSON.

Installation
$ npm install -g mockapi
Usage / Getting Started
Simply run mockapi from within a working directory, run npm install, and your api is bootstrapped and ready to go:

$ cd /path/to/your/mockapi/project
$ mockapi
$ npm install
Creating your own routes
While the included "Hello World" route is crazy awesome, you're bound to want to build in your own routes. It is your API, after all!

You can create all of your routes in the routes directory. For convenience, all routing modules in that directory are loaded by default into the routes variable in app.js. All you need to do is create your route definitions via express:

routes/myRoute.js

exports.get = function(req, res){
  res.json({ foo: "bar" });
};
app.js

app.get('/my/route', routes.myRoute.get);
Run the server
No surprise here, just run app.js through node:

$ node app.js