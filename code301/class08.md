# reading 08

## APIs

1. What does REST stand for?

   - REST API : REST stands for Representational state transfer.

2. REST APIs are designed around a \_\_\_\_.

   - REST APIs are designed around resources, which are any kind of object, data, or service that can be accessed by the client.

3. What is an identifer of a resource? Give an example.

   - A resource has an identifier, which is a URI that uniquely identifies that resource.

4. What are the most common HTTP verbs?

   - The most common operations are GET, POST, PUT, PATCH, and DELETE.

5. What should the URIs be based on?

   - On nouns (the resource) and not verbs (the operations on the resource).

6. Give an example of a good URI.

   - `https://adventure-works.com/orders` Good
   - `https://adventure-works.com/create-order` Bad

7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

   - are those that expose a large number of small resources.
   - Such an API may require a client application to send multiple requests to find all of the data that it requires. This procedure will cause a
     load on the server and it is not what we want.

8. What status code does a successful GET request return?

   - a successful GET method typically returns HTTP status code 200 (OK)

9. What status code does an unsuccessful GET request return?

   - an unsuccessful GET the resource cannot be found, the method should return 404 (Not Found).

10. What status code does a successful POST request return?
    - If a POST method creates a new resource, it returns HTTP status code 201 (Created).
11. What status code does a successful DELETE request return?
    - a successful DELETE method return HTTP status code 204.
