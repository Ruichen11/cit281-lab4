![world](https://user-images.githubusercontent.com/84296093/120625767-db26a680-c416-11eb-85da-0d2cbd0acb07.jpg)

# cit281-lab4
Purpose of this lab:
- Create fastify Node.js web server, add fastify to project using npm. 
- Add git repo 
- add a second route with query parameters, test and commit. 

### Lab Code:
```
// Require the Fastify framework and instantiate it
const fastify = require("fastify")();
// Handle GET verb for / route using Fastify
// Note use of "chain" dot notation syntax
fastify.get("/", (request, reply) => {
  reply
    .code(200)
    .header("Content-Type", "text/html; charset=utf-8")
    .send("<h1>Hello from Lab 4!</h1>");
});

// Name Route
fastify.get("/name", (request, reply) => {
    const {first, last} = request.query;
    const name = first && Last ? `${first} ${last}` : 'Guest';
    reply
      .code(200)
      .header("Content-Type", "text/html; charset=utf-8")
      .send(`<h1>Hello, ${name} </h1>`);
  });

// Start server and listen to requests using Fastify
const listenIP = "localhost";
const listenPort = 8080;
fastify.listen(listenPort, listenIP, (err, address) => {
  if (err) {
    console.log(err);
    process.exit(1);
  }
  console.log(`Server listening on ${address}`);
});
```
![Lab 4](https://user-images.githubusercontent.com/84296093/120625600-baf6e780-c416-11eb-8e5c-ac72be8246be.JPG)

#### What I learned:
- Practiced how to efficiently use git from command prompt. Learned how to request object query property to display on web-server.


[Sourcecode](https://ruichen11.github.io/Ruichen11.CIT-Minor/)
