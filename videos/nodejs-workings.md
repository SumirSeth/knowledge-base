---
title: 'How Node.js works?'
description: 'A video on the workings of node.js by Piyush'
video: 'https://youtu.be/y0aTs56DJWk'
tags: ['backend', 'node', 'nodejs', 'coding', 'working']
source: 'Piyush Garg'
---

# How Node.js works?

- The flow starts from the <u>**client**</u>.

- Clients make a request to the server.

- The requests are queued in an <u>**event queue**</u>.

- The <u>**event loop**</u> *watches* the event queue to assign to workers.

- There are two operations that a request can be operated as:
  
  - Blocking (sync)
  
  - Non Blocking (async)

- Non Blocking simply processes the request and sends a response.

- To resolve blocking operation, a thread pool is approached.

- Numerous threads are assigned some work and these threads resolve the blocking operation.

- Threads *sit* in the thread pool.
