# Unhandled Promise Rejection in Node.js Server

This repository demonstrates a common error in Node.js applications: unhandled promise rejections.  An asynchronous operation within an HTTP server isn't properly handled, leading to server crashes. The solution shows how to use a `try...catch` block or properly handle rejections in promises to prevent this.

## Bug
The `bug.js` file contains a Node.js server with an asynchronous operation that randomly either resolves or rejects a promise.  The rejection case lacks proper error handling, causing the server to crash when the promise is rejected.

## Solution
The `bugSolution.js` file demonstrates the proper way to handle this scenario using a `try...catch` block or using `.catch()` to prevent crashes. The server now gracefully handles both successful and failed asynchronous operations.