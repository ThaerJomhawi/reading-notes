# Read : Class 13 - CRUD

## Status Code

it's a part of the response returned by the server when a client (e.g., a browser) calls a URL. With the help of a status code, the server tells the client whether the request was successfully processed or whether an error occurred.

- 100s = Information responses
- 200s = Successful responses
- 300s = Redirection messages
- 400s = Client error responses
- 500s = Server error responses

## QUES:

#### What is a status code 202:

202 Accepted


#### What is a status code 308:

**308 Permanent Redirect**
403 code

#### What code would you use if an update didn’t return data to a client:

400s => Client error responses

#### What code would you use if a resource used to exist but no longer does:

404 - Not Found

#### What is the ‘Forbidden’ status code:

403 code

#### 

## Build A REST API With Node.js, Express & MongoDB (Video):

- Why do we need to pull our MongoDB database string out of our server and put it into our .env?

To deploy our application.

- What is middleware?

Code that runs once the server got the request but before passed to the route

- What does app.use(express.json()) do?

Let our server accept json as a body inside a post element or get element ...etc

- What does the /:id mean in a route?

This means its parameter and used to get all parameters passed after the slash

- What is the difference beween PUT and PATCH?

PUT update all info (replace info), PATCH update only specific item (modify).

- How do you make a defalut value in a schema?

inside schema value add default: THE VALUE YOU WANT TO BE DEFAULT

- What does a 500 error status code mean?

There is error on server

- What is the difference between a status 200 and a status 201?

201 says specifically that you created something, but 200 says success only (201 code used in post request)
