# What are Web Applications
A web application (web app) is an application program that is stored on a remote server and delivered over the internet through a browser interface.

# Challenges for moden web applications
- **consume services** from another system
- **provide services** to anoter system
- **modularize** my application (to manage complexity)
- respond to multiple **overlapping (asynchronous) requests**
- make changes **persistent** (for large, distributed systems
- allow and restrict **user access** (security and privacy)
- **display information** from a source
- **Synchronize information** shown on different views
- maximize **responsiveness**
- **adapt** to different devices and screen sizes

# Reference Model

![alt text](https://miro.medium.com/v2/resize:fit:1400/1*3E4w7rCe3eaz6gLlZoe6nQ.png)

*this is slightly different from the reference model in the lecture slides, but it has most of the key features*

# Protocol Layers

![alt text](https://www.imperva.com/learn/wp-content/uploads/sites/13/2020/02/OSI-7-layers.jpg)

for us the **application layer** is what we are concerned about. This is the HTTP protocol and is how we communicate between applications.

# Overview of HTTP

**HTTP messages are how data is exchanged between a server and a client**, there are two types of messages:
- requests: sent by the client to trigger an action on the server
- responses: the answer from the server

**HTTP messages are composed of textual inforimation encoded in ASCII** and span over mutliple lins. In HTTP/1.1 and earlier versions of the protocol these messages were onpenly sent across the connection.

## Uniform Resource Identifiers
- **URI** (Uniform Resource Identifier)
- - String of characters to identify (name or name and location) resource
- **URL** (Uniform Resource Locator)
- - A URI that also specifies the means of action upon, or obtaining representation. That is, a URI with access mechanism and location
- **URN** (Uniform Resource Name)
- - Depricated: historical name for URI

## URL Breakdown

![alt text](https://media.geeksforgeeks.org/wp-content/uploads/20210625160610/urldiag.PNG)

## HTTP Headers

**Distinguish between**
- General Headers (required)
- Entity Headers (apply to the body of the request)
- Request headers
- Response Headers

**Cookies are implemented with headers**
- Set-Cookie: <...> (int the header of the server's HTTP response
- Cookie: <...> (in the header of subsequent client http req)

**Use headers to**
- Maintain session
- Personalise
- Track

# HTTP Requests
