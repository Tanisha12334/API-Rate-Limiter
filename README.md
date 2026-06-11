# API Rate Limiter Service

## Overview

API Rate Limiter Service is a backend application built using Java and Spring Boot that restricts the number of requests a user can make within a specified time window. The project helps prevent API abuse, excessive traffic, and server overload.

## Features

* IP-based request tracking
* Fixed Window Rate Limiting
* Maximum 5 requests per 60 seconds
* Automatic counter reset after 60 seconds
* HTTP 429 (Too Many Requests) responses
* JSON-based API responses
* Built using Spring Boot REST APIs

## Tech Stack

* Java 21
* Spring Boot
* Maven
* REST APIs
* HashMap Data Structure

## How It Works

1. User sends a request to the API endpoint.
2. The application identifies the user's IP address.
3. Request count is tracked using a HashMap.
4. If requests exceed 5 within 60 seconds:

   * HTTP 429 status code is returned.
   * JSON error response is sent.
5. After 60 seconds, the request count resets automatically.

## API Endpoint

### GET /hello

Example Success Response:

```json
{
  "message": "Request Allowed"
}
```

Example Error Response:

```json
{
  "message": "Too Many Requests!"
}
```

## Project Structure

```text
src
├── controller
│   └── HelloController.java
├── model
│   └── ApiResponse.java
```

## Concepts Implemented

* Spring Boot Controllers
* REST APIs
* HTTP Status Codes
* JSON Responses
* HashMap
* Request Tracking
* Fixed Window Rate Limiting

## Future Enhancements

* Redis-based distributed rate limiting
* User authentication support
* Configurable request limits
* Database persistence
* Dashboard for monitoring API traffic

## Author

Tanisha Javalkar
B.Tech Computer Science and Systems Engineering
