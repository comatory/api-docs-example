# Introduction to REST API

## What is REST API?
REST (Representational State Transfer) API is a popular architectural style for designing networked applications. It uses standard HTTP methods to perform operations such as GET, POST, PUT, DELETE on resources.

## Key Concepts
1. **Resource**: In REST, everything is considered as a resource, which can be a data entity or object. Resources are accessed using URIs.
   
2. **HTTP Methods**:
   - `GET`: Used to retrieve information from the server.
   - `POST`: Used to create a new resource on the server.
   - `PUT`: Used to update an existing resource on the server.
   - `DELETE`: Used to remove a resource from the server.
   
3. **Status Codes**:
   - `200`: OK - Successful request.
   - `201`: Created - Resource successfully created.
   - `400`: Bad Request - Invalid request.
   - `404`: Not Found - Resource not found.
   
4. **Headers**:
   - `Content-Type`: Specifies the format of the request/response payload.
   - `Authorization`: Contains credentials for authentication.

## Examples

### GET Request
- **Endpoint**: `/api/users`
- **Description**: Retrieve a list of users.
- **Example**:
  ```http
  GET /api/users HTTP/1.1
  Host: api.example.com
  Authorization: Bearer your_token_here
  ```
- **Response**:
  ```json
  [
    { "id": 1, "name": "Alice" },
    { "id": 2, "name": "Bob" }
  ]
  ```

### POST Request
- **Endpoint**: `/api/users`
- **Description**: Create a new user.
- **Request Body**:
  ```json
  { "name": "Charlie", "email": "charlie@example.com" }
  ```
- **Example**:
  ```http
  POST /api/users HTTP/1.1
  Host: api.example.com
  Content-Type: application/json
  Authorization: Bearer your_token_here

  { "name": "Charlie", "email": "charlie@example.com" }
  ```
- **Response**:
  ```json
  { "id": 3, "name": "Charlie", "email": "charlie@example.com" }
  ```

## Conclusion
REST APIs are widely used for building web services that can be easily consumed by client applications. Understanding the basic concepts and using standard HTTP methods can help in designing efficient and scalable APIs.
