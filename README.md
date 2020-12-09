# Simple-Web-App

This repository is a little practice with NodeJS, Express and JS provided by Brian Holt tutorial at FrontEndMasters.
Before to start, you have to install [NodeJS](https://nodejs.org/en/) to provide the basic tools to create the server. 
Once it's installed, we have to install Express (NodeJS framework) by the following way ```npm install express```.

### Server.js
Firstly, we include *express* and *path* modules. *Path* is a library for getting correct file locations.
 - ```const app = express()```: creates the server.
 - ```getRandomComplemen()```: returns a random item from complements array.
 - ```app.get("/", callback)```: it does reference to the home page, in this case, http://localhost:3000
    - ```res.sendFile(path.join(__dirname, "index.html"))```: sends to user the ```index.html``` file. 
        - __dirname:  is a Node variable that's the folder of where the server.js file is.
 - ```app.get("/complement", callback)```: it does reference to http://localhost:3000/complement.
    - ```res.json({ complement: getRandomComplement() }).end()```: this is the response to the request with a JSON object. It shows an object with one key: complement.
 - ```app.use("/public", express.static("./public"))```: serves everything in the public directory publicly(in this case, only the complements.js file)
