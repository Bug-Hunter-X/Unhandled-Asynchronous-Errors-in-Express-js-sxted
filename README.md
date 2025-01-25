# Unhandled Asynchronous Errors in Express.js

This repository demonstrates a common error in Express.js applications: unhandled errors within asynchronous route handlers.  Asynchronous operations (like database queries or external API calls) often use callbacks or promises. If these operations throw errors and are not properly handled, the server might crash unexpectedly.

## The Problem

The `bug.js` file shows a simple Express.js server with a route that simulates an asynchronous operation.  There's a 50% chance the operation will throw an error.  Because this error isn't caught, the server will crash if the error is thrown.

## The Solution

The `bugSolution.js` file demonstrates the proper way to handle errors in asynchronous routes using `try...catch` blocks within the asynchronous operation or by handling errors within the promises.