# Understanding basics of API

![api](https://github.com/user-attachments/assets/29620d07-b843-4261-93f9-3348043245e1)

## What is an API?

An API (Application Programming Interface) allows different software applications to communicate with each other. It defines a set of rules and protocols for building and interacting with software applications.

## Types of APIs

1. **REST (Representational State Transfer)**
   - Uses standard HTTP methods.
   - Stateless and scalable.
   
2. **SOAP (Simple Object Access Protocol)**
   - Uses XML for messaging.
   - Provides higher security with WS-Security.

3. **GraphQL**
   - Allows clients to request only the data they need.
   - Reduces the number of API calls.

4. **gRPC (Google Remote Procedure Call)**
   - Uses HTTP/2 for transport.
   - Supports multiple programming languages.

## The Four Pillars of an API

### 1. Endpoint

An endpoint is a specific URL where an API can access resources. It represents the location from which APIs can access the required resources.

Example:
```bash
https://api.example.com/
```

### 2. Path

The path specifies the specific resource or action within an API endpoint.

Example:
```bash
https://api.example.com/users
```

### 3. Parameters

Parameters are used to pass data to the API. They can be:

- Path Parameters: Used to identify specific resources
  
 Example:
 ```bash
 https://api.example.com/users/{userId}
 ```

- Query Parameters: Used to filter or modify the response

 Example:
 ```bash
 https://api.example.com/users?name=john
 ```

- Body Parameters: Used to send data in the body of the request (usually for POST, PUT requests).

 Example: JSON payload in a POST request
 ```bash
 {
   "name" = "Gojo Satoru"
 }
 ```

### 4. Authentication

Authentication ensures that the API is accessed securely by authorized users. Common methods include:

- API Key: A unique key provided to the user.

- OAuth: Token-based authentication.

- Basic Auth: Base64 encoded username and password.

## Various Request Methods

### 1. GET

Retrieves data from the server.

Example:
```http
GET https://api.example.com/users
```

### 2. POST

Submits data to the server.

Example:
```http
POST https://api.example.com/users
```
```bash
//Content-Type: application/json

{
  "name": "Gojo Satoru",
  "email": "gojo@example.com"
}
```

### 3. PUT

Updates whole existing data in collection.

Example:
```http
PUT https://api.example.com/users/{userId}
```
```bash
//Content-Type: application/json

{
  "name": "New Gojo Satoru",
  "email": "gojo2@example.com"
}
```

### 4. PATCH

Updates partial existing data in collection.

Example:
```http
PATCH https://api.example.com/users/{userId}
```
```bash
//Content-Type: application/json
{
  "name": "Gojo Satoru",
  "email": gojo2@example.com"
}
```

### 5. DELETE

Deletes data from the server.

Example:
```http
DELETE https://api.example.com/users/{userId}
```

## Platforms for API Handling

1. **Postman**
   - A popular tool for testing and verifying APIs.
   - Allows for automated testing and documentation.
   
2. **Insomnia**
   - A user-friendly API client.
   - Supports GraphQL, REST, and SOAP.

3. **Swagger**
   - Provides a comprehensive suite for API development.
   - Automatically generates API documentation.

4. **cURL**
   - A command-line tool for making HTTP requests.
   - Useful for quick API testing.
