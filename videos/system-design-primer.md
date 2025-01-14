---
title: 'System Design Basics'
description: 'A playlist from Gaurav Sen on system design basics.'
video: 'https://www.youtube.com/playlist?list=PLMCXHnjXnTnvo6alSjVkgxV-VH6EPyvoX'
playlist: 'https://www.youtube.com/playlist?list=PLMCXHnjXnTnvo6alSjVkgxV-VH6EPyvoX'
tags: ['coding', 'system design', 'system', 'design', 'gaurav sen', 'backend']
source: 'Gaurav Sen'
---

# <i>(vid 1)</i> System Design Primer

The video is based on an example of a "pizza parlor". He starts by assuming there is only one (1) chef serving all the pizzas.

Obviously, this system does not ***scale*** at all. Using this example, he goes over ways to make the ==system scalable==.

## Vertical Scaling

- Ask the chef to work harder.

- In technical terms, <u>optimise processes and increase throughput using the **same resource**</u>.

  Same ways to optimise would be to make the paste in advance, in technical terms, using cron jobs to automate and optimise - *preprocessing*.

## Backup Servers

- Incase the chef does not come, have a backup chef.
- In technical terms, in computers we have a master and a slave architecture.

## Horizontal Scaling

- Buy more chefs.
- In tech terms, get more servers of approx same properties.

## Microservices

- Imagine you have three chefs, two of them are specialized in making pizzas(1 and 3) and one has a specialty in garlic breads(2).
- You would assign orders in a way where all the garlic bread orders would *route* to chef 2.
  And all the pizza orders would go to chef 1 and 3.
- Anytime you need an update on garlic breads, you only have to get updates from one particular group.

## Distributed System

-  Imagine the electricity goes out. Your business stops for that day.
- A distributed system adds a huge amount of complexity in a way where you set "clones" of the main system (which could be smaller than the main one) in different areas.
- An advantage this gives is that although the distributed system is less capable than the main one, it would serve nearby orders or requests faster than if it had to go to the main server.

## Load Balancing

- A central place that routes requests intelligently.
- This central place is the *Load Balancer*.

## Decoupling a system

- Decouple the different aspects of the system. Pretty simple.

## Logging and Metric Calculation

- While making a system, you want to be taking logs such that you always have an idea of things especially when they go wrong.

## System Extensibility

- Make the system such that it could be extended at any wanted moment.

---

# <i>(vid 2)</i> Horizontal vs Vertical Scaling

Intro: Suppose you have some algorithm on a cloud server. People are paying you to use that algo. After sometime, you face scalability and reliability issues. What's the possible solutions?

|       Horizontal        |        Vertical         |
| :---------------------: | :---------------------: |
| Load balancing Required |           N/A           |
|        Resilient        | Single point of failure |
|                         |                         |
|                         |                         |

  