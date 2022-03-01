# Lab 7 - Flask

## Question 0: What is the URL of your python flask_restfull code on github???
https://github.com/dlallan/cmput404-lab7-flask

## Question 1: How are Flask and Django different? What does Django provide for you that Flask does not?
Although Flask and Django are both web development frameworks for Python, they have many different features. Notably, Django supports Model-View-Template (MVT) web applications, and provides an object relational mapper (ORM) for automatically mapping Python objects to database tables in the backend. 

In contrast, Flask is a much simpler server framework. It does require the user to follow any one architectural style, and does not offer an ORM out-of-the-box. Users would have to implement those features themselves, or take on third-party dependencies.

## Question 2: What does REST stand for? When I say something is RESTful, what does that mean?
REST stands for REpresentational State Transfer. When something is called RESTful, it means it embodies the qualities of REST architecture. This means that the API was architected with the following features:
* Stateless (all state in the request)
* Resources are uniformly accessible by name/ID in URLs (server endpoints)
* HTTP verbs (e.g. GET, PUT, DELETE, POST) correspond to cacheable operations the client can perform on a resource

## Question 3: What does CRUD stand for? For each letter in CRUD, give the associated HTTP method.
CRUD stands for Create, Read, Update, Delete. These operations correspond to the following HTTP methods:
* Create -> POST or PUT
* Read -> GET
* Update -> POST, PUT, or PATCH
* Delete -> DELETE

## Question 4: What do HTTP 1XX Status Codes mean? HTTP 2xx? HTTP 3xx? HTTP 4xx? HTTP 5xx?
* 1XX -> Informational codes
* 2XX -> Success codes
* 3XX -> Redirection codes
* 4XX -> Client error codes
* 5XX -> Server error codes

## Question 5: What is an XSS attack? Provide one way a site can be vulneratble to an XSS attack.
A cross-site script (XSS) attack is when malicious scripts are injected into a website. The scripts are then run by other users visiting the website, exposing their cookies and other private information to the script.

A website can be vulnerable to XSS attacks if it accepts raw text input in its forms. An attacker can include their script as the input to a form field, and a vulnerable website could then store the script in the backend.

## Question 6: What does CORS stand for? What situation in web application development will you need to implement CORS protection? Hint: What does the CO part of CORS mean?
CORS stands for Cross-Origin Resource Sharing. CORS is feature of HTTP that allows a server and client decide on any origins the client can safely send additional requests to after loading a resource from the main request origin.

This feature is available by setting HTTP headers like `Origin`, `Access-Control-Allow-Origin`, `Access-Control-Request-Method`, `Access-Control-Request-Headers`, `Access-Control-Allow-Credentials`, and `Access-Control-Max-Age`.

CORS protection should be considered for any website or web application that needs to restrict resource sharing to a predefined set of origins. For example, a web service that is supposed to be for company use only can use CORS to restrict requests to origins only belonging to an allow-list of company domains and subdomains.
