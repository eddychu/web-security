# Atonamy of a Modern Web Application

Most web applications today can be characterised more properly as two or more applications communicating via a network protocol. 

Those applications can be connected with a REST API. 

The UI is more akin to traditional desktop application. Web apps today manage their own life cycle loops, request their own data, and do not require a page reload after the initial bootstrap is complete.

The single web client may communicate with multiple servers. Image hosting application will have a seperated hosting server for static files, while manage other servers for databases and logins.

A modern web app typically employs the following tech stack:

1. Rest API / graphql api.
2. JSON or XML.
3. Frontend JavaScript frameworks.
4. Local data store on the client (cookies, web storage, indexDB)
5. An authentication and authorization system (oauth)
6. One or more linux web servers.
7. backend server softwares (ExpressJS, Apache, Nginx)
8. One or more databases. (sql or nosql)


Technology that on the horizon:

1. Cache API for storing requests locally.
2. Web sockets as an alternative network protocol for client to server/ client to client communication.
3. Web assembly, which allow non-JavaScript to be used for writing client-side code in the browser.

---


