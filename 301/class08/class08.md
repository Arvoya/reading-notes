[[301/README|Module 301]]
# APIs Best Practices

Reading assignment for Class 08

## Questions & Answers

[RESTful web API design](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design)

1. What does REST stand for? Representational State Transfer
2. REST APIs are designed around a resources.
3. What is an identifier of a resource? The URI
4. What are the most common HTTP verbs? GET, POST, PUT, PATCH, DELETE
5. What should the URI's be based on? nouns or resource
6. Give an example of a good URI. 'https://adventure-works.com/orders'
7. What does it mean to have a 'chatty' web API? Is this a good or a bad thing? APIs that expose a large number of small resources. Generally considered inefficient, as it can lead to higher loads and slower performance.
8. What status code does a successful `GET` request return? 200
9. What status code does an unsuccessful `GET` request return? 404
10. What status code does a successful `POST` request return? 201
11. What status code does a successful `DELETE` request return? 204

## RESTful web API design

### What is REST?

> In 2000, Roy Fielding proposed Representational State Transfer (REST) as an architectural approach to designing web services. REST is an architectural style for building distributed systems based on hypermedia. REST is independent of any underlying protocol and is not necessarily tied to HTTP. However, most common REST API implementations use HTTP as the application protocol, and this guide focuses on designing REST APIs for HTTP.

* **REST (Representational State Transfer):** An architectural style for building distributed systems based on hypermedia. Independent of any underlying protocol, commonly using HTTP.
* **Distributed Systems:** A network of independent computers that appears to its users as a single coherent system.
  * **Multiple Components:** Located on different networked computers, which communicate and coordinate their actions by passing messages to one another.
  * **Resource Sharing:** Resources (like files, databases) can be shared across the network.
  * **Scalability:** Can easily scale horizontally (adding more machines) rather than vertically (upgrading hardware on a single machine).
* **Hypermedia:** This is an extension of the term hypertext, which is a way of structuring information through links (hyperlinks) within a network of interconnected nodes (like webpages). Hypermedia extends hypertext by including a wider range of media types like: text, images, videos, and audio. All interconnected through hyperlinks. 

### Key Principles of RESTful APIs

* **Resource-Based:** APIs centered around resources (objects, data, services) that are accessible to the client.
* **Uniform Interface:** Utilization of standard HTTP methods (GET, POST, PUT, PATCH, DELETE) for operations.
* **Stateless Operations:** Each request contains all necessary information, independent of other requests.
* **Resource Identification through URIs:** Resources are uniquely identified using URIs. Example: 'https://adventure-works.com/orders'
* **Protocol-Independent:** REST can be used over different protocols, not just HTTP.

### Design Considerations for RESTful APIs

* **Platform Independence:** Support for various client platforms using standard protocols.
* **Service Evolution:** Ability to evolve without breaking existing clients. Emphasis on discoverability of functionalities.
* **Consistent Naming and Resource Handling:** Logical organization of RUIs and a focus on business entities rather than database structure.
* **Limit Resource Load:** Avoid chatty APIs; denormalize data when necessary for efficiency. Excessive requests can lead to inefficiency and increased load on the server. Design the API to reduce the number of requests needed for a client to complete a task.


### HTTP Method Usage in RESTful APIs

* **GET:** To retrieve resources.
  * Returns 200 (OK) for success
  * Returns 404 (Not Found) if the resource is not found.
* **POST:** To create new resources or submit data.
  * Returns 201 (Created) for successful creation.
  * Returns 204 (No Content) for no result to return.
  * Returns 400 (Bad Request) if client puts invalid data into the request
* **PUT:** To create or replace resources.
  * Returns 200 (OK)
  * Returns 204 (No Content)
  * Returns 409 (Conflict) might not be possible to update an existing resource.
* **PATCH:** To partially update resources.
  * Returns 415 (Unsupported Media Type) Patch document format isn't supported.
  * Returns 400 (Bad Request) Malformed patch document.
  * Returns 409 (Conflict) Patch document valid, but changes can't be applied to the resource in current state.
* **DELETE:** To remove resources.
  * Returns 204 (No Content) delete operation is successful
  * Returns 404 (Not Found) resource never existed.

### Versioning and Asynchronous Operations

* **Versioning:** Managing API changes to support different client application versions.
* **Asynchronous Operations:** Handling long operations without latency, returning a status for ongoing processes.

### HATEOAS (Hypermedia as the Engine of Application State)
* **Principle:** Clients interact dynamically with a service through hyperlinks provided in responses.
* **Implementation:** Includes links in responses to navigate and discover available operations related to resources.

### Additional Concepts

* **URIs (Uniform Resource Identifiers):** Strings used to identify resources, encompassing URLs (Uniform Resource Locators) and URNs (Uniform Resource Names).
  * **URL vs URI:**
    * **URL:** A specific type of URI that, in addition to identifying a resource, provides a means to locate it on the network. For example, 'https://www.example.com/page'
    * **URI:** More broad, can be either a locator (URL), a name (URN), or both. For example, 'mailto:example@example.com' is URI but **not** a URL.
* **Open API Initiative:** Standardization of REST API descriptions for interoperability and promoting a contract-first design approach.
