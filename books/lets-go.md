---
title: Let's Go!
description: A book on creating fast, secure and maintainable web applications using go.
tags: ['web', 'server', 'backend', 'go']
author: ['Alex Edwards']
---

# Let's Go!

Jotting down important pieces of information as I traverse through the book.

## 1. Introduction

### 1.1 Prerequisites

- Goes through the pre-requisites such as installing go, setting it up and general knowledge such as terminals.

---

## 2. Foundations

### 2.1 Project Setup and creating a module

- Important to know what modules mean in go.

- Conventions about naming modules. Preferably, have URLs you own as the name of the module.

- If the module has to be available to everyone, give the name such that it points to the location from where people can download it.

### 2.2 Web Application Basics

- Three essentials of web app
  
  - Handler : Responsible for executing app logic and for writing http response headers and bodies.
  
  - Router : **<u>Known as *servemux*</u>** in go term. Stores a mapping between the URL patters for application and corresponding handler. <u>Usually, only one servemux</u> is there for an app.
  
  - Web Server.

- <span style="color:#26B66E">Note : </span> Go's servemux treats the url pattern "/" like a catch-all.

- The *TCP Network Address* that is passed in `http.ListenAndServe()` is in the form of `host:port`. One can omit the host. One can also use a *named port* for ex: `:http`. Go will look for it in `/etc/services`.

### 2.3 Routing Requests

- Concept of **<u>fixed paths</u>** and <u>**Subtree path**</u>.

- Fixed paths *dont* end with a trailing slash

- Subtree paths do.

- Eg: `/snippet/view` is a fixed path.

- Fixed path => Exact Match required

- `/` is a subtree path.

- Subtree path => start of the URL path is matched.

- <span style="color:#26B66E">Note : </span> there is something called `http.HandleFunc()` which basicaly allows one to register routes without declaring servemux.
  Behind the scenes, this is basically using something like `DefaultServeMux() = NewServeMux()`.
  <span style="color:#cc3948">Caution : </span> De


