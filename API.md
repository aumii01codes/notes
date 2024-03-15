An **Application Programming Interface (API)** is a contract that allows code to talk to other code. APIs are the building blocks of modern software because they allow for sharing of resources and services across applications, organizations, and devices.<br>
APIs are not just for developers. API use is not limited to the tech and IT industries. Everyone benefits from APIs either directly or indirectly because APIs make processes more efficient and connect the services we love and rely on.<br>

Imagine, API to be the waiter in a restaurant who serves as the connection between the customers (clients) and cook in the kitchen (server).
- Client is the requester. Ex: browser, web app, mobile app
- API is the implified interface for interacting with the backend
- Server is the backend where the processing happens

Architecture types to build Api:
REST (Representational State Transfer)
GraphQL
WebSockets
webhooks
SOAP (Simple Object Access Protocol)
gRPC (Google Remote Procedure Call)
MQTT (MQ Telemetry Transport)

Various types of API based on medium:
Hardware APIs
Interface for software to talk to hardware.
Example: How your phone's camera talks to the operating system. 
Software Library APIs
Interface for directly consuming code from another code base.
Example: Using methods from a library you import into your application.
Web APIs
Interface for communicating across code bases over a network.
Example: Fetching current stock prices from a finance API over the internet.

Various types of API based on scope:
Public APIs (aka Open APIs)
Consumed by anyone who discovers the API
Private APIs
Consumed only within an organization and not made public
Partner APIs
Consumed between one or more organizations that have an established relationship

Postman is an API platform for building and using APIs. Postman simplifies each step of the API lifecycle and streamlines collaboration so you can create better APIs faster and consume them with ease. That's why Postman is trusted by over 25 million users worldwide!

cURL : client uniform resource locator

In the API-first world:
- APIs are considered a #1 priority
- APIs are easily consumable
- APIs are easily discoverable

API USED IN THIS COURSE WILL BE Public, Rest, web API

REST APIs
Some traits of REST APIs include not storing session state between requests, the ability to cache, and the ability to send and receive various data types.
Collections are places to organize your API requests in Postman.

Anatomy of a Request:
Method
Endpoint/path
Parameters
Headers
Body


METHOD
It mentions the operation that we want to perform
When we make an HTTP call to a server, we specify a request method that indicates the type of operation we are about to perform. These are also called HTTP verbs.
REST API allows you to CRUD (Create, Read, Update, Delete)
Method to perform these operations:
- GET = Retrieve data (Read)
- POST = Send data (Create)
- PUT/PATCH* = Update data (Update)
- DELETE = Delete data (Delete)


GET



POST



PUT


PATCH


DELETE




ENDPOINT
the url on which the method is performed
In addition to a request method, a request must include a request URL that indicates where to make the API call. A request URL has three parts: a protocol, host (location of the server), and path (route on the server). In REST APIs, the path often points to a reference entity, like "books".
Protocol 
Host
Path
https://
library-api.postmanlabs.com
/books

Paths and complete URLs are also sometimes called API endpoints.

PARAMETERS
Query parameter
Some APIs allow you to refine your request further with key-value pairs called query parameters.
Query parameters are added to the end of the path. They start with a question mark (?) followed by the key-value pairs in the format: <key>=<value>.  If there are multiple query parameters, each is separated by an ampersand (&). This can alos be done under the Params tab with setting the key & value and Postman syncs the changes made to the request URL

Path Variable
Another way of passing request data to an API is via path variables (path parameters). A path variable is a dynamic section of a path and is often used for IDs and entity names such as usernames. The path variable comes immediately after a slash in the path. For example, the GitHub API allows you to search for GitHub users by providing a username in the path in place of {username} below: GET https://api.github.com/users/{username}
You can have multiple path variables in a single request, such as this endpoint for getting a user's GitHub code repository: GET https://api.github.com/repos/{owner}/{repoName}

Note: Some API documentation uses colon syntax to represent a wildcard in the path like /users/:username, while some use curly braces like /users/{username}. They both mean the same thing: that part of the path is dynamic!
