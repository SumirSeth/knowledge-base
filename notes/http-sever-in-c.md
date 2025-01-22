---
title: 'Building an HTTP Server in C'
description: 'My personal experience and guide to building an http server in C'
tags: ['coding', 'programming', 'http', 'server', 'c', 'guide', 'blog']
---

# Building an HTTP Server in C: My experience.

## Understanding basics of HTTP

- **<u>HTTP is a protocol</u>** for communication usually between a client like browser and a server.
- A server listens to incoming connections, processes requests, and sends back response.
- At the minimum, this project should be able to handle GET requests and respond with plain text or HTML.

Research the basics of the structure of an HTTP Server.

What does a HTTP request look like?

What does a minimal response look like?

The answer to above questions must be clear before getting started.

## Learn about sockets in C (or in general).

- Sockets allow communication between programs over a network.

- A minimal server involves, 

  1. Creating a socket.
  2. Binding it to a port.
  3. Listening for incoming requests.
  4. Accepting and handling those connections.

Look into `socket()`, `bind()`, `listen()`, `accept()`.

## Decide the workflow

- Set up a socket.
- Wait for a connection.
- Receive the request.
- Parse the http request.
- Send back a basic http response (start with sending a hello world blank page).

Break this into smaller parts. Can you write a small program to create a socket and print when it receives a connection?

> The above things should be clear before starting to build a http server.

---

## Anatomy of HTTP Communication

1. HTTP Request.

   An http request from a client contains:

   1. **Request Line**: Specifies the HTTP method, target resource, protocol versions.

      ``` bash
      GET /index.html HTTP/1.1
      ```

      - Method: Specifies the action (`GET`, `POST`, `PUT`, `DELETE`)
      - Resource: The path to the requested resource. (`/index.html`).
      - HTTP Version: The protocol version (`HTTP/1.1` or `HTTP/1.0`).

   2. **Headers**: Key value pairs providing meta data.

      ```makefile
      Host: example.com
      User-Agent: Mozilla/5.0
      Content-Type: text/html
      ```

   3. Optional Body: For methods like `POST`.

      ```makefile
      GET / HTTP/1.1
      Host: localhost:3000/
      User-Agent: curl/7.68.0
      ```

2. HTTP Response

   An https response from the server contains.

   1. **Status Line**: Specifies the HTTP version, status code and a message.

      ```bash
      HTTP/1.1 200 OK
      ```

      - Version: HTTP Version
      - Status Code: Numeric code indicating the outcome (`200`, `500`)
      - Message: A short description of the status.

   2. **Headers**: Key value pairs providing metadata about the response.

      ```les
      Content-Type: text/html
      Content-Length: 13
      ```

   3. **Body**: The actual data sent to client.

      ```mak
      HTTP/1.1 200 OK
      Content-Type: text/html
      Content-Length: 13
      
      Hello, World!
      ```

## Key Feature of HTTP Servers

- Stateless Protocol: Each request-response pair is independent; the server doesn’t retain state between requests.
- Port Numbers
- Persistent Connections: By default, HTTP/1.1 keeps connections open for multiple requests unless explicitly closed.

## Responsibilities of a HTTP Server (basic)

1. Listen on a specific IP and Port.
2. Accept connections.
3. Read the http request.
4. Parse the request.
5. Generate an HTTP response.
6. Send the response back.
7. Close the connection.