---
title : 'Coding Highly Scaleable Backend | System Design'
description: 'A video by Piyush Garg coding a node.js backend server that handles processes asyncronously using concept of queues.'
video: https://www.youtube.com/watch?v=02YpQGNmRwI
tags: ['system design', 'system', 'design', 'coding', 'backend', 'piyush garg', 'queues', 'queue', 'scaling']
source: 'Piyush Garg'
---

# Scalable Backend Using Concept of Queues

The video goes over the concepts of scaling your backend in a real world scenario.

## Concepts:

- <u>**Horizontal Scalling**</u> : When you scale by increasing the number of servers. You distribute workload across servers.

- <u>**Vertical Scalling**</u>: When you scale by increasing processing attributes (RAM and memory for example) of a particular server.

- <u>**Critical and Non Critical Tasks**</u> : Tasks that are important and need to be done IMMEDIATELY are critical tasks, whereas non-critical task can be pushed off to a queue bus system.

- <u>**Queue**</u> : Data Structure that operate on the principle of FIRST IN FIRST OUT (FIFO). Useful as job queues or task queues. Queues enhance system efficiency and reliability by letting processes handle tasks at their own pace without blocking main workflows.

- <u>**Producer and Consumer (or Worker) in Queues**</u> : A producer is something that pushes events or jobs to the queue while the worker resolves the job.

- [**Aiven**](https://aiven.io/) : An open source database solution. It provides easy access to tools to develop infrastructures.

- <u>**Redis**</u> : Open-source, in-memory data structure store often used as a **database**, **cache**, and **message broker**. Great for Queues and Job Management.

## Learnings:

- Horizontal Scalling is not that good because it takes time to boot new servers/machines that will offload the tasks.

- In that time interval, users will face tremendous amounts of lag or the service might even crash.


---