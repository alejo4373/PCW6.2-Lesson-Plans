# Lesson Plan: Express. Passing Data

## Exit ticket asks:
* Different ways to send additional data to the server
* Where are request url parameters populated in Express
* Where are query parameters populated in Express
* POST request characteristics and limitations

## Anticipating Fellow Needs:

1. What will fellows be most likely to struggle with and why? 
  * When to use query strings vs url params.
  * Request body encoding.
  * Query string syntax. `?` `key=value`

2. What simpler assignment will you give to a struggling fellow: 
  * Scan urls of website you are familiar with and find query strings used as well as what you think might be a route parameter.
  * Inspect a POST request in Postman or in the network tab of Chrome dev tools. What headers do you see? Where is the body data?

3. What challenge assignment will you give to a fellow who is following along and ready for the next step: 
  * Research how to handle a file upload in Express.js and implement a simple profile photo upload for a server that registers users.

## Lesson Breakdown

### Motivation
  * Send data to the server?
  * Learn a few different ways of doing it.
  * Only getting data is not fun. You want to add, create & amend resources. 
  * [Question] Why do we want to pass data to the server?

### Ways of passing data to a Server
  * Some ways are better suited for some cases
  * URL Parameters: Variables sections in the URL path. like `/users/<user_id>` 
  * URL Query strings: Commonly used for filtering/sorting information or specifying details. They come in key-value pairs after a question mark in the url.
  * Request Body: Safer and for larger amounts of data.

### URL Parameters
  * Allow you endpoints/routes to be dynamic
  * Variables sections in the URL path. like `/users/<user-id>` 
  * [DEMO] Canvas students urls. What do we see stay the same? What do we se changing?
  * [QUESTION] If instagram.com's server were build using Express.js, What would their routes look like?
  * How do we handle this in Express?. i.e. `app.get('/:parameter_name')`
  * [DEMO] Server with route `/dog/:breed`
  * Inspect `req.params`
  * [ACTIVITY] P1

### URL Query Strings
  * Commonly used for filtering/sorting information or specifying details.
  * Key-value pairs after a question mark in the url.
  * Are always at the end of the endpoint.
  * [DEMO] Query params used in the CatAPI https://docs.thecatapi.com/api-reference/images/images-search
  * How do we handle this in Express. Well, we don't express does it automatically.
  * [ACTIVITY] P2
  * [QUESTION] What are query strings the pokemon api allows. Does instagram allow query parameters?
  * How do we handle this in Express?. Well express does it for us. `req.query`
  * [DEMO] Server that returns a subset of an array.
  * [TODO] Change demo on and example on lesson
  * [TODO] Link express docs

### Request Body
  * Used to create or update a resource on the server.
  * Used for sensitive information. Also for large amounts of data.
  * Created often via form submissions or file uploads.
  * Body data travels can be of a few different types/different formats. `x-www-form-urlencoded`, `json`
  * [DEMO] Inspect a POST request. Username and passwords or Twitter post
  * POST request body
    * Never cached
    * Not in browser history
    * Unable to be bookmarked
    * No restriction on body length
  * [ACTIVITY] N1
  * How do we handle this in Express. We need a body parser.
    * Install and setup `body-parser`
    * Inspect `req.body`
    * [DEMO] Route for adding a new dog.
  * [TODO] Complement lesson on what methods allow requests body and which one don't

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
