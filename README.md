 1) npm init -y            => Initialize npm 
 
 2) npm i json-server      => install npm
 
 3) create server.js       => for database creation (db.json)
 
 4) copy template to server.js    => 
 *************************************************************
 const PORT = process.env.PORT || 3001;
const path = require("path");
const jsonServer = require("json-server");
const server = jsonServer.create();
const router = jsonServer.router(path.join(__dirname, "db.json"));
const middlewares = jsonServer.defaults();
server.use(middlewares);
server.use(jsonServer.bodyParser);
server.use("", router);
server.listen(PORT, () =>
  console.log(`JSON Server is running on port ${PORT}`)
);
*****************************************************************
 5)  node server.js  => db.json is created 