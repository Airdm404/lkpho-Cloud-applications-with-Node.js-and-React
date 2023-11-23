**Repo**
- Create express server and run it
- Work on Middlewares with Express server
- Use middleware and JWT for authentication
- Render a static HTML page through express server


**Create express server from scratch with nodemon**

* myexpressapp = name of server
  - mkdir myexpressapp
  - cd myexpressapp

* npm init

* npm install express --save

* add sample code to index.js
  - `const express = require('express');
const app = new express();
const port = 8080;

app.get("/", (req,res) => {
    return res.send("Hello World!");
});

let server = app.listen(port, () => {
    console.log("listening at http://localhost:"+ port)
})` 


* make changes in package.json to start the server with npm start. include **start** under scripts
  - `{
  "name": "myexpressapp",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "node index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^X.X.X"
  }
}`

* run npm start. add other endpoints and have fun

*  to have the server restart after changes
  - run npm install --save-dev nodemon
  - change your start in package.json to use nodemon
  - `{
  "name": "myexpressapp",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start" : "nodemon index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^X.X.X"
  },
  "devDependencies": {
    "nodemon": "^X.X.X"
  }
}`
- run npm start
