# 11/09/21: Client-Server Communication

- A **server** runs code/provides information/communicates with the **clinet** by sending **protocols**
- Protocol tell the code what you requested in a certain way, which is returned by the server 
- Dispatch tree takes a route based on request of path and type 
- Generally, server is disployed in the cloud and client is the app on a user's device
- Most of the web requests are **get requests**
- Fun fact: 404 Error is thrown when the server is asked for something it doesn't have
- **To avoid lag and a slow app, we need to implement callbacks**