# HTTP & REST APIs

## What is JSON and why is it used?
- JSON (JavaScript Object Notation) is a lightweight text format for storing and exchanging data.
-  Despite the name, it's used across virtually all programming languages, not just JavaScript.
- It represents data using simple, human-readable structures.
- Basic building blocks if JSON are Objects, Arrays and Values.

It is used widely because:

 1. Human-readable and easy to write
 2. Language-independent
 3. Lightweight
 4. Maps naturally to data structures
 5. Standard for web APIs
 6. Used for configuration and storage

## How does it differ from regular JavaScript objects?
- JSON and Javascript may seem different but it is fundamentally different.
- JSON is a text format or a string format whereas javascript is a live in memory data structure.
- Think of JS like a real room with furniture which we can interact with and think of JSON as the photograph of that room where we can only see and not interact with it.

## Why is JSON used so widely in APIs instead of formats like XML or plain text?
- XML needs opening, closing tags, etc for everything whereas JSON's brackets and commas are far more easier data to transmit, parse, and store, which matters a lot.
- JSON understands numbers, booleans, and null as actual types whereas XML treats everything as a text.
- Parsing is simpler and faster in JSON whereas its more complex with XML.
- Plain text doesn't scale for structured data with JSON.
- 

# Explore a Public REST API 
## API TESTING REPORT - ReqRes API
ReqRes API tested using Postman

Base URL: https://reqres.in/api
Authentication: x-api-key 

1. The HTTP method used: GET


The request URL: https://reqres.in/api

The status code of the response: 200 OK


The response body (JSON):
```JSON
{ 
    
     "page": 2,
    "per_page": 6,


    "total": 12,
    "total_pages": 2,
    "data": [
        {
            "id": 7,
            "email": "michael.lawson@reqres.in",
            "first_name": "Michael",
            "last_name": "Lawson",
            "avatar": "https://reqres.in/img/faces/7-image.jpg"
        },
        {
            "id": 8,
            "email": "lindsay.ferguson@reqres.in",
            "first_name": "Lindsay",
            "last_name": "Ferguson",
            "avatar": "https://reqres.in/img/faces/8-image.jpg"
        },
        {
            "id": 9,
            "email": "tobias.funke@reqres.in",
            "first_name": "Tobias",
            "last_name": "Funke",
            "avatar": "https://reqres.in/img/faces/9-image.jpg"
        },
        {
            "id": 10,
            "email": "byron.fields@reqres.in",
            "first_name": "Byron",
            "last_name": "Fields",
            "avatar": "https://reqres.in/img/faces/10-image.jpg"
        },
        {
            "id": 11,
            "email": "george.edwards@reqres.in",
            "first_name": "George",
            "last_name": "Edwards",
            "avatar": "https://reqres.in/img/faces/11-image.jpg"
        },
        {
            "id": 12,
            "email": "rachel.howell@reqres.in",
            "first_name": "Rachel",
            "last_name": "Howell",
            "avatar": "https://reqres.in/img/faces/12-image.jpg"
        }
    ],
    "support": {
        "url": "https://benhowdle.im/first-cto-playbook?utm_source=reqres&utm_medium=json&utm_campaign=referral",
        "text": "Become a better CTO. A playbook of painful stories and practical advice from a two-time startup CTO."
    },
    "_meta": {
        "powered_by": "ReqRes",
        "docs_url": "https://app.reqres.in/documentation",
        "upgrade_url": "https://app.reqres.in/upgrade",
        "example_url": "https://app.reqres.in/examples/notes-app",
        "variant": "v1_a",
        "message": "Your data persists here. Add auth, logs, and custom schemas to build a real backend.",
        "cta": {
            "label": "See example app",
            "url": "https://app.reqres.in/examples/notes-app"
        },
        "context": "legacy_success"
    }
}
```

2. The HTTP method used: POST


The request URL: https://reqres.in/api

The status code of the response: 200 Created


The response body (JSON):

```JSON
{
    "id": "805",
    "createdAt": "2026-07-09T05:21:14.579Z",
    "_meta": {
        "powered_by": "ReqRes",
        "docs_url": "https://app.reqres.in/documentation",
        "upgrade_url": "https://app.reqres.in/upgrade",
        "example_url": "https://app.reqres.in/examples/notes-app",
        "variant": "v1_a",
        "message": "Your data persists here. Add auth, logs, and custom schemas to build a real backend.",
        "cta": {
            "label": "See example app",
            "url": "https://app.reqres.in/examples/notes-app"
        },
        "context": "legacy_success"
    }
}
```

## Reflect on What You Observed
### What is the difference between GET, POST, PUT, and DELETE?
----
### 1. GET
This is used for retrieve/read data. Doesn't change anything on the server.
Real world use cases: 
- Used for fetching bank balance
- Used for refreshing your instagram feed
- Used for fetching a product page on instagram

### 2. POST
 To create a new resource, or submit data that causes a change.
 Real world use cases:
 - Signing in a new account
 - Commenting on a post
 -  Ordering something online
 
 ### 3. PUT
 To update or replace an existing resource entirely.
- Editing your profile
- Changing a shipping address

### 4. DELETE
To remove a resource.
- Deleting a post on social media
- Deleting a file 
- Removing something from your cart

### What are the major categories of HTTP status codes, and why do they matter? 
1. Informational

The request was received and it is still processing. This is rarely seen.
```
   eg: 100 Continue
```
2. Success

The request works.
```
   eg: 200 OK — Standard success 
       201 Created — A new resource was successfully created
       204 No Content — Worked but nothing returns
```
3. Redirection

Request is in process but more actions will be needed to complete it.  
```
   eg: 301 Moved Permanently — Resource has a new permanent URL
       304 Not Modified — Still valid
```
4. Client Error

There's an error in your request.
```
   eg: 400 Bad Request — Malformed request

       401 Unauthorized — Missing or invalid api key.

       403 Forbidden — It is authorised but cannot be accessed.

       404 Not Found — Resource doesn't exist

```

5. Server Error

Something's wrong on the server's side.
```
     eg: 500 Internal Server Error — Server crash or bug

         503 Service Unavailable — Server is overloaded or down for 
         maintenance
```

### What are headers in HTTP? What’s one header you observed during your API testing, and why is it important?

- Headers in HTTP are key-value pairs that are sent along with request that carry extra data other than the data that is in the actual body.

- One header I observed during API testing is ``` x-api-key```.

- This header important as this is a custom header used mainly for api authentication.

## Key Takeaways
- How APIs work: APIs act as a bridge between client and server. The client sends a request  and the server processes it and responds with data and a status code. 

- What's important in an HTTP request: A request needs the right method, correct URL, proper headers and a valid body. Missing even one piece causes the whole request to fail.

- How understanding HTTP helps as a developer: Understanding HTTP makes it much easier to debug errors, build efficient integrations with third-party services, and design your own APIs in a way that's predictable and easy for other developers to use the same.
