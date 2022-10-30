# Book-API
A REST API to manage books with Node.js and Express.

Introduction
REST APIs are an industry-standard way for web services to send and receive data. They use HTTP request methods to facilitate the request-response cycle and typically transfer data using JSON, and more rarely - HTML, XML and other formats.

In this guide, we are going to build a REST API to manage books with Node.js and Express.

For the sake of simplicity, we won't be using a database, so you don't need experience using one. We will use a simple JavaScript array to store our data instead.

What is a REST API?
REST (Representational State Transfer) is a standard architecture for building and communicating with web services. It typically mandates resources on the web are represented in a text format (like JSON, HTML, or XML) and can be accessed or modified by a predetermined set of operations. Given that we typically build REST APIs to leverage with HTTP instead of other protocols, these operations correspond to HTTP methods like GET, POST, or PUT.

On a collection of data, like books for example, there are a few actions we'll need to perform frequently, which boil down to - Create, Read, Update and Delete (also known as CRUD Functionality).

An API (Application Programming Interface), as the name suggests, is an interface that defines the interaction between different software components. Web APIs define what requests can be made to a component (for example, an endpoint to get a list of books), how to make them (for example, a GET request), and their expected responses.

What is Express?
ExpressJS is one of the most popular HTTP server libraries for Node.js, which by default isn't as friendly for API development. Using Express, we simplify API development by abstracting away the boilerplate needed to set up a server, which makes development faster, more readable and simpler. You can spin up a prototype API in seconds and a couple of lines of code.

Although it's primary use was to simplify things with sensible defaults, it's highly customizable using functions called "middleware".


Note: Express is very lightweight and is built on top of middlleware. Using middleware, you can expand and extend its functionality beyond the functions already present by default.

Even though we are only going to build a REST API in this guide, the ExpressJS framework is not limited to just that - hosting static files, performing server-side rendering, or even using it as a proxy server isn't uncommon and the sky's the limit with additional middleware.

HTTP Request Types
There are a few types of HTTP methods that we need to grasp before building a REST API. These are the methods that correspond to the CRUD tasks:

POST: Used to submit data, typically used to create new entities or edit already existing entities.
GET: Used to request data from the server, typically used to read data.
PUT: Used to completely replace the resource with the submitted resource, typically used to update data.
DELETE: Used to delete an entity from the server.

Note: Notice that you can use either POST or PUT to edit stored data. You're free to choose whether you even want to use PUT since it can be omitted fully. Though, stay consistent with the HTTP verbs you use. If you're using POST to both create and update, then don't use the PUT method at all.

What We are Going to Build
Let's create a simple app to store information about books. In this app, we will store information about the ISBN of the book, title, author, published date, publisher and number of pages.

Naturally, the basic functionality of the API will be CRUD functionality. We'll want to be able to send requests to it to create, read, update and delete Book entities. Of course, an API may do much more than this - provide users with an enpoint to get statistical data, summaries, call other APIs, etc.

Non-CRUD functionalities are application-dependent, and based on your project's nature, you'll probably have other endpoints. However, practically no project can go without CRUD.

To avoid making up book data - let's use a dataset from GitHub to get some sample details about books.
