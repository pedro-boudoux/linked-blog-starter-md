**Class:** [[CIS*1050]]
**Date:** 10-04-2025
**Topics:**  

*HTTP* or *HyperText Transfer Protocol* is the protocol used to transfer web resources. *HTTP* allows for communication between a variety of hosts and clients and supports a mixture of network configurations. *HTTP* is a stateless protocol, communication usually takes place over TCP/IP.

## URLs
At the heart of the web, communications is the request message, which is sent via *Uniform Resource Locators*, or *URLs*. *URLs* have a simple structure, for example:

![[Pasted image 20250410165610.png]]

## Verbs
*URLs* reveal the identity of the particular host with which we want to communicate with, but the action that must performed on the host is specified via *HTTP Verbs*.


| Verb   | Purpose                                                                                                                        |
| ------ | ------------------------------------------------------------------------------------------------------------------------------ |
| GET    | Fetch an existing resource. The URL contains all the necessary information the server needs to locate and return the resource. |
| POST   | Create a new resource. POST requests usually carry a payload that specifies the data for the new resource.                     |
| PUT    | Update an existing resource. The payload may contain the updated data for the resource.                                        |
| DELETE | Delete an existing resource.                                                                                                   |
## Sending Messages
Basically, the client sends a request to the server containing the URL and a verb (representing the action to be performed). The server processes the request and sends back a status code and a message body.

The request or response message has the following generic structure (just for information purposes):
```js
message = <start-line>
*(<message-header>)
CRLF
[<message-body>]
```

## Status Codes
Once a request has been made, the server responds with status codes and message payloads. The *status code* is important and tells the client how to interpret the server response. 

### 1xx Informational Messages
(new to HTTP/1.1): This tells the client to continue sending the remainder of the request.

### 2xx Successful
This tells the client that the request was successfully processed. The most common code is `200 OK`.

### 3xx Redirection
This requires the client to take additional action. The most common use-cache is to jump to a different URL to fetch the resource.

### 4xx Client Error
These codes are used when the server thinks that the client is at fault, either by requesting an invalid resource or making a bad request. These are the most common codes:


| Code | Name               | Meaning                                                                                                                                |
| ---- | ------------------ | -------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad Request        | The request was malformed.                                                                                                             |
| 401  | Unauthorized       | Request requires authentication.                                                                                                       |
| 403  | Forbidden          | The server has denied access to the resource.                                                                                          |
| 404  | Not Found          | The resource does not exist.                                                                                                           |
| 405  | Method Not Allowed | Invalid HTTP verb used in the request line, or the server does not support that verb.                                                  |
| 409  | Conflict           | The server could not complete the request because the client is trying to modify a resource that is newer than the client's timestamp. |
### 5xx Server Error
This class of codes are used to indicate a server failure while processing the request.