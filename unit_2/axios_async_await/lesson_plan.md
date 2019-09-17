# Axios & Async-Await

## Motivation
  * Predictable, and intuitive API
  * Simple setup
  * Automatic parsing of JSON
  * Cross environment (node & browser)

## Setup
  * Import script in html head

## Using Axios
  * First axios get request fetching `https://fsw62-todos-api.herokuapp.com/api/todos`
  * *Exercise*: What differences do you see between `fetch` and `axios`. What do they share?
    - Axios: Only one `.then` needed
    - Axios: Automatic parsing of json 
    - Axios: How we specify the request method `.get`, `.post`
    - Axios: Is an exteranal module. Fetch is built into the browser.
    - Both return promises
    - Both need at least one `.then` & one `.catch`\
  * Posting data with Axios
    - POST request todo to `https://fsw62-todos-api.herokuapp.com/api/todos`
    - POST request with axios vs fetch

## Async & Await

### Async
  * Async keyword in front of any function makes the function automatically return a promise
  * returnOne with and without async
  * attach a `.then(alert)`

### Await
  * Keyword to wait for a promise to be settled. Can only be used inside an `async` function.
  * *Exercise*: `fireRequest` async function making get request without await console.log(response). What did you get in the console
  * Now include the `await` keyword before `axios.get()`

### Error handling 
  * **Exercise** What happens if our promise rejects? Change the url to make the promise fail and share what you find.
  * `try` & `catch`
  * instead of `.catch` we wrap our await in a `try`
  *  A try...catch statement marks a block of statements to try, and specifies a response, should an exception be thrown.

### Chaining calls
  * Example. 
    - Creating a todo.
    - Marking the todo as completed.
    - Deleting the todo.

## End
* Look at the example in the lesson and recreate it. Do not copy and paste code. Make sure you understand by asking peers and instructors.
