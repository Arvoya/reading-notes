# CRUD
[Module 301](./301)

Reading assignment for Class 12.

## Questions & Answers

[Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

1. In your own words, describe what each group of status code represents:
	* 100's = Informational status codes
	* 200's = Success codes
	* 300's = Redirection codes
	* 400's = Client error codes
	* 500's = Server error codes
2. What is a status code 202? Asynchronous process started
3. What is a status code 308? Permanent Redirect
4. What code would you use if an update didn't return data to a client? 204
5. What code would you use if a resource used to exist but no longer does? 410
6. What is the 'Forbidden' status code? 403
--- 

[Build A REST API With Node.js, Express, & MongoDB - Quick (Video)](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env? Because the mongodb string has the username and password, also good practice for security purposes.
2. What is middleware? Code that runs when server gets a request, but before it gets passed to a route. 
3. What does `app.use(express.json())` do? lets server accept JSON as a body instead a Post element or Get element
4. What does the `/:id` mean in a route? it means it is a parameter
5. What is the difference between `PUT` and `PATCH`? Patch will only update what the user passes vs updating everything all at once
6. How do you make a default value in a schema? you add the type of value or exact value like a boolean of `true`.
7. What does a `500` error status code mean? Error on the server side.
8. What is the difference between a status `200` and a status `201`? 201 means successfully created an object, its a bit more specific in creating something vs 200.

## HTTP Status Codes

### 100-199

Informational status codes. 

### 200-299

Success codes.

### 300-399

Redirection codes.

### 400-499

Client error codes.

### 500-599

Server error codes.

### Custom Classes

Classes above 599, not conventional but can find out in the wild.

## CRUD 

* Create
* Read
* Update
* Delete

### Create

#### Status Codes

* 200 OK
* 201 Created
* 202 Accepted - Often used for **asynchronous** processing, so tells clients request was valid, but will finish after sometime.
* 303 See Other  - Similar to `202` but uses a `location` header field to inform client the location in which to find the actual status of the creation process.

### Read

#### Status Codes

* 200 OK
* 206 Partial Content - Used with a `Range` header field in the request denoting content is too big to be delivered in one response.
* 300 Multiple Choices - Redirect used if multiple representations for one resource and the client has to choose one
* 308 Permanent Redirect - Tells client to use another URL to access resource and not use the current URL anymore.
* 304 Not Modified - client redirected to its locally cached representation from a previous read.
* 307 Temporary Redirect - URL to a resource could change in the future, and client should ask the current URL before accessing the real one.

### Update

#### Status Codes

* 200 OK
* 204 No Content - Proper code for updates that don't return data
* 202 Accepted - Asynchronous update. Should include a URL to access the updated resource once the update is complete.

### Delete

#### Status Codes

* 200 OK
* 204 No Content 
* 202 Accepted - Asynchronous

