 
 # What does REST stand for?

 REST is an architectural style for building distributed systems based on hypermedia. REST is independent of any underlying protocol and is not necessarily tied to HTTP. However, most common REST API implementations use HTTP as the application protocol, and this guide focuses on designing REST APIs for HTTP

 # REST APIs are designed around a ____.
 resources, which are any kind of object, data, or service that can be accessed by the client.
 # What is an identifer of a resource? Give an example.
 resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:

**HTTP**
`
https://adventure-works.com/orders/1
`
# What are the most common HTTP verbs?
- GET retrieves a representation of the resource at the specified URI. The body of the response message contains the details of the requested resource.
- POST creates a new resource at the specified URI. The body of the request message provides the details of the new resource. Note that POST can also be used to trigger operations that don't actually create resources.
- PUT either creates or replaces the resource at the specified URI. The body of the request message specifies the resource to be created or updated.
- PATCH performs a partial update of a resource. The request body specifies the set of changes to apply to the resource.
- DELETE removes the resource at the specified URI.
# What should the URIs be based on?
resource URIs should be based on nouns (the resource) and not verbs (the operations on the resource).
# Give an example of a good URI.
`
https://adventure-works.com/orders //
`
# What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
"chatty" web APIs that expose a large number of small resources. Such an API may require a client application to send multiple requests to find all of the data that it requires. Instead, you might want to denormalize the data and combine related information into bigger resources that can be retrieved with a single request. However, you need to balance this approach against the overhead of fetching data that the client doesn't need. Retrieving large objects can increase the latency of a request and incur additional bandwidth costs. For more information about these performance antipatterns, see Chatty I/O and Extraneous Fetching.
# What status code does a successful `GET` request return?
A successful GET method typically returns HTTP status code 200 (OK). If the resource cannot be found, the method should return 404 (Not Found).
# What status code does an unsuccessful `GET` request return?

a GET request to the URI listed above might return this response body:

JSON
`
{"orderId":1,"orderValue":99.90,"productId":1,"quantity":1}
`
# What status code does a successful `POST` request return?
If the client puts invalid data into the request, the server should return HTTP status code 400 (Bad Request). The response body can contain additional information about the error or a link to a URI that provides more details.
# What status code does a successful `DELETE` request return?
If the delete operation is successful, the web server should respond with HTTP status code 204 (No Content), indicating that the process has been successfully handled, but that the response body contains no further information. If the resource doesn't exist, the web server can return HTTP 404 (Not Found).

![](https://external-preview.redd.it/BKh0eTbme9gp6gvJ2U4Hlps6WjJl33nPJPRaC_bdzKs.jpg?auto=webp&s=566fc0beca8fdc0082b57ebde9883c77e670a528)
![]()
![]()





