# WRRC and Java

## HTTP Request

### *The HTTP Request Lifecycle:*

1. Local Processing: 

* The browser extract the protocol, host , and optional port number, resource path, and query strings that are described in form.
* then the browser will look for the URL .

2. Resolve an IP

* the server will look for the IP address and will get some more information 

3. Establish a TCP Connection

* ordering the needed information by writing a sequence number for each byte sent 
* connections are opened using what’s known as a three-way handshake.

4. Send an HTTP Request

* send a request made from request line + request head 
* one the server receives  the request it creates HTTP response 
* the first byte the client receives should have a head HTTP  

5. Tearing Down and Cleaning Up

* the client send a FIN that the server response to, then send its own FIN , then the client waits and cant receive calls 
* the browser now processing  what it got 


# Simple HTTP Request

* Http url connection helps us to do http request without using additional libraries all of these are part of java.net but in this way the code can be more complicated.
  
* we can use the method `Open connection ()` this method can establish connection object but not the connection.
* The HttpUrlConnection class is used for all types of requests by setting the requestMethod attribute to one of the values: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.

  