## REST API Testing Interview Questions
### Easy Questions:
1. What is REST API?

 - Answer: REST (Representational State Transfer) is an architectural style for designing networked applications. It relies on stateless, client-server communication and uses standard HTTP methods (GET, POST, PUT, DELETE, etc.) for operations.

2. What are the common HTTP methods used in RESTful services?

 - GET: Retrieve information from the server.
 - POST: Send data to the server to create a resource.
 - PUT: Update an existing resource on the server.
 - DELETE: Remove a resource from the server.  
 - PATCH: Partially update a resource on the server.

3. What is the difference between PUT and POST methods?

 - PUT: Idempotent operation used to update a resource or create it if it does not exist.
 - POST: Non-idempotent operation used to create a new resource.

4. What is a status code in REST API? Give some examples.

Status codes indicate the result of the HTTP request. Examples include:

 - 200 OK: The request was successful.
 - 201 Created: The request was successful and a new resource was created.
 - 400 Bad Request: The server could not understand the request due to invalid syntax.
 - 404 Not Found: The server could not find the requested resource.
 - 500 Internal Server Error: The server encountered an error and could not complete the request.

5. What is JSON?

 - JSON (JavaScript Object Notation) is a lightweight data-interchange format that is easy to read and write for humans and easy to parse and generate for machines.

6. How do you validate JSON response in REST API testing?

 - JSON responses can be validated using libraries like jsonschema in Python or built-in assertions in tools like Postman to check the structure, data types, and values.

7. What is an API endpoint?

 - An API endpoint is a specific URL where an API can access the resources it needs to perform its functions. It consists of a base URL and a resource path.

8. What is the purpose of API authentication?

 - API authentication ensures that only authorized users can access or manipulate the API resources, thus providing security and protecting sensitive data.

9. What are query parameters in REST API?

 - Query parameters are key-value pairs that are appended to the endpoint URL to pass additional information to the server, often used for filtering, sorting, or pagination.

10. What tool can be used for manual REST API testing?

 - Postman is a popular tool for manual REST API testing, allowing users to send HTTP requests and inspect responses.

### Moderate Questions:
1. How do you handle API versioning?

API versioning can be handled by:
 - Including the version number in the URL (e.g., /api/v1/resource).
 - Using a version parameter in the query string or headers (e.g., Accept: application/vnd.myapi.v1+json).

2. What is the difference between SOAP and REST?

 - SOAP: Protocol that relies on XML-based messaging and is known for its rigid standards and built-in error handling.
 - REST: Architectural style that uses standard HTTP methods and is typically more lightweight and easier to use with various data formats like JSON.

3. How do you handle rate limiting in REST API testing?

 - Rate limiting can be tested by sending multiple requests to the API in quick succession and verifying that the server responds with the appropriate status code (e.g., 429 Too Many Requests) once the limit is exceeded.

4. How do you use Postman to test REST APIs?

 - Create a new request in Postman.
 - Specify the HTTP method and URL.
 - Add headers, query parameters, and request body if needed.
 - Send the request and inspect the response.

5. What is an API gateway?

 - An API gateway is a server that acts as an API front-end, handling requests, routing them to the appropriate services, and performing functions like authentication, rate limiting, and load balancing.

6. How do you perform authentication in REST API testing?

Authentication can be performed using methods like:
 - Basic Authentication (using username and password).
 - Token-based Authentication (e.g., JWT).
 - OAuth.

7. How do you validate XML responses in REST API testing?

 - XML responses can be validated using libraries like xmlschema in Python or built-in assertions in tools like SoapUI to check the structure, data types, and values.

8. What is CORS and how do you handle it in API testing?

 - (Cross-Origin Resource Sharing) is a security feature implemented by browsers to restrict web pages from making requests to a different domain. In API testing, ensure the server includes appropriate CORS headers (Access-Control-Allow-Origin) in the response.

9. What is Swagger/OpenAPI?

 - Swagger (now part of the OpenAPI initiative) is a framework for defining APIs using a standard, language-agnostic interface. It helps in documenting APIs and generating client/server code.

10. How do you test REST APIs using JMeter?

 - Add a Thread Group to your test plan.
 - Add an HTTP Request sampler to the Thread Group.
 - Configure the HTTP Request sampler with the API endpoint and parameters.
 - Add listeners like View Results Tree to inspect responses.

### Difficult Questions:
1. How do you automate REST API testing using a framework like RestAssured?

 > import io.restassured.RestAssured;
import io.restassured.response.Response;
import static io.restassured.RestAssured.*;
import static org.hamcrest.Matchers.*;
public class APITest {
public void testGetRequest() {
RestAssured.baseURI = "https://api.example.com";
given().queryParam("key", "value")
.when().get("/endpoint")
.then().statusCode(200).body("data.id", equalTo(1));
}
}

2. How do you handle OAuth 2.0 authentication in REST API testing?

 > Response response = given()
.auth()
.oauth2("accessToken")
.when()
.get("https://api.example.com/endpoint");
response.then().statusCode(200);

3. How do you use mocks/stubs for REST API testing?

Tools like WireMock can be used to create mocks/stubs for REST APIs. This helps in simulating API responses for testing without hitting the actual server.
 > WireMockServer wireMockServer = new WireMockServer(8080);
wireMockServer.start();
wireMockServer.stubFor(get(urlEqualTo("/api/resource"))
.willReturn(aResponse().withStatus(200).withBody("response body")));

4. How do you perform data-driven testing for REST APIs?

 - Data-driven testing can be performed by using data from external sources (CSV, Excel, databases) and parameterizing API requests. Tools like RestAssured or Postman collections can be used for this purpose.

5. What is HATEOAS and how is it implemented in REST APIs?

HATEOAS (Hypermedia as the Engine of Application State) is a constraint of REST that allows clients to dynamically navigate resources using hyperlinks provided in the responses. It is implemented by including links in the API responses.
 > {
"data": { "id": 1, "name": "Example" },
"_links": {
"self": { "href": "/api/resource/1" },
"next": { "href": "/api/resource/2" }
}
}

6. How do you perform security testing for REST APIs?

 - Security testing involves checking for vulnerabilities like SQL injection, cross-site scripting (XSS), and ensuring proper authentication and authorization mechanisms are in place. Tools like OWASP ZAP and Burp Suite can be used for security testing.

7. How do you handle pagination in REST API testing?

Test pagination by sending requests with query parameters like page and limit, and validate that the response includes the correct data and pagination metadata.
 > given().queryParam("page", 1).queryParam("limit", 10)
.when().get("/api/resource")
.then().statusCode(200).body("data.size()", equalTo(10));

8. What are idempotent and safe methods in REST APIs?

 - Safe methods: Methods that do not alter the server state (e.g., GET, HEAD).
 - Idempotent methods: Methods that produce the same result if called multiple times (e.g., GET, PUT, DELETE).

9. How do you implement error handling and validation in REST APIs?

Implement comprehensive error handling by returning appropriate status codes and error messages for different scenarios. Validate input data using schema validation and provide meaningful error responses.
> {
"status": 400,
"message": "Invalid request",
"errors": [
{ "field": "username", "message": "Username is required" }
]
}

10. How do you measure the performance of REST APIs?

 - Use tools like JMeter, Gatling, or LoadRunner to measure the performance of REST APIs by simulating concurrent users and requests, and analyzing metrics like response time, throughput, and error rates.