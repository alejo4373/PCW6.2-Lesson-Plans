# Lesson Plan: Express. Middleware

## Exit ticket asks:
* Why to use middleware
* How to add middleware to an express app
* Callbacks as core concept for middleware
* How is the next middleware invoked

## Anticipating Fellow Needs:

<!-- 1. What will fellows be most likely to struggle with and why? 
  * When to use query strings vs url params.
  * Request body encoding.
  * Query string syntax. `?` `key=value`

2. What simpler assignment will you give to a struggling fellow: 
  * Scan urls of website you are familiar with and find query strings used as well as what you think might be a route parameter.
  * Inspect a POST request in Postman or in the network tab of Chrome dev tools. What headers do you see? Where is the body data?

3. What challenge assignment will you give to a fellow who is following along and ready for the next step: 
  * Research how to handle a file upload in Express.js and implement a simple profile photo upload for a server that registers users.
 -->
## Lesson Breakdown

### Motivation
  * Middleware is a core concept of express.
  * Plugin like paradigm.
  * Perform additional work on every request. Like parsing body or time stamp it, log it.

### What is Middleware?
  * We think of server like a computer program. It takes some input, does some work and produces and output. That we call request and response.
  * Middleware are functionality executed between a request and a response.
  * Walk though lesson diagram.

### Basic Middleware in a Route
  * Middleware are just functions. They receive `res`, `req` and `next`.
  * [QUESTION] Where have we seen something similar?
  * Callbacks we pass to our routes. Are sometimes refereed to as Route Handler or Request Handler
  * This callbacks can in fact be considered middleware. Why because the callback can signal that is done to express by invoking `next()`
  * Upon a middleware invoking `next()`, Express calls the next middleware in the chain until some middleware sends a response with on of the sender methods in the response such as `res.json()` or `res.send()`.
  * [DEMO] Let's see it. Lesson demo & login verification. 
  * [ACTIVITY] Input validation.

### App-Wide Middleware
  * We have been using this already. `cors` and `body-parser` are middleware.
  * [DEMO] Implement `cors` ourselves.
  * [ACTIVITY] Create app-wide middleware that logs the method, endpoint and time of a request. Implement `morgan`

## Activities for this lesson 
Describe in detail. What are the instructions you will give? What will be the example you offer? How long will fellows spend on each component? How will you wrap up the activity?

* P1. In pairs: Go to the pokemon api https://pokeapi.co/docs/v2.html and find what you believe are route/url parameters. Discuss why you think something may or may not be a url parameter. Share what you find.

* P2. In pairs: Find query strings/params and their meaning used in the craigslist's for sale section. https://newyork.craigslist.org/search/sss. Try a few filters on the left.

* N1. With neighbors. Talk to the people near you about scenarios that use a POST request. What would the request body contain?. Try to inspect a few of them. Share with the class. What scenarios you weren't fully sure. What scenarios did you find?

### Schedule: 

### 1
* Time: 07:00 - 08:00 pm
* Instructors Are: Pass through lesson material while asking them to implement the small examples.
* Fellows are: Listening, asking questions

### Possible questions
* [When to use URL params over URL Query strings?](https://stackoverflow.com/questions/30967822/when-do-i-use-path-params-vs-query-params-in-a-restful-api)


## Resources
* [URI Syntax standard - RFC3986](https://tools.ietf.org/html/rfc3986#section-3.4)
* [HTTP Methods and status code that allow a body](https://stackoverflow.com/questions/16339198/which-http-methods-require-a-body)
* [HTTP Message Spec](https://www.w3.org/Protocols/rfc2616/rfc2616-sec4.html#sec4)
* [How does uploading a file to a server works](https://stackoverflow.com/questions/8659808/how-does-http-file-upload-work)
