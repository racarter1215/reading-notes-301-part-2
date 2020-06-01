# Node

### Node.js is a JavaScript runtime built on google chrome’s V8 js engine

##### Stack Overflow says it's an event-based, non-blocking, asynchronous I/O runtime that uses google chrome’s V8 js engine and libuv library.

### The V8 engine

##### V8 engine: an open-source JavaScript engine that runs in google chrome and other Chromium-based web browsers

##### Node takes the V8 engine and enhanced it with various features, such as a file system API, an HTTP library, and a number of operating system–related utility methods.

##### In essence, Node is a JavaScript runtime

##### You can check that Node is installed on your system by opening a terminal and typing node -v. After this, something like v12.14.1 is displayed. This is the current LTS version at the time of writing.

##### Since you only target the specific V8 engine you have, you can write your js in the latest syntax and can avoid many compatability issues. 

##### NPM is the world's largest software registry.

##### to install globally, type: npm install -g jshint

##### If one opens the package.json file on a project that has node modules in the root, you’ll see lodash listed under the dependencies field. By specifying your project’s dependencies in this way, you allow any developer anywhere to clone your project and use npm to install whatever packages it needs to run.

##### Node.js is used to automate the process of developing a modern JavaScript application.

##### These build tools include bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.

##### You need to understand Node to start developing apps with any modern JavaScript framework like React or Angular

##### Node.js lets us run JavaScript on the server.

##### Node.js is single-threaded and event-driven, which means that everything that happens in Node is in reaction to an event. This ensures that information is processes more efficiently and stops slowdowns and site crashes.

##### Node’s execution model causes the server very little overhead, and consequently it’s capable of handling a large number of simultaneous connections. The traditional approach to scaling a Node app is to clone it and have the cloned instances share the workload. 

### Downsides of Node.js

##### What to avoid: blocking I/O calls, CPU-intensive operations, and errors should always be handled correctly for fear of crashing the entire process. Others dislike the callback coding style.

##### Sample Code:
###### const http = require('http');

###### http.createServer((request, response) => {
######   response.writeHead(200);
######   response.end('Hello, World!');
###### }).listen(3000);

###### console.log('Server running on http://localhost:3000');

