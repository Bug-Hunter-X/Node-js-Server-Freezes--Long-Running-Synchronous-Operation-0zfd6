# Node.js Server Freeze Bug

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler can freeze the server, making it unresponsive to new requests. The `bug.js` file contains the buggy code, and `bugSolution.js` provides a solution using asynchronous operations.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `node bug.js`.
4. Attempt to make multiple requests to `http://localhost:3000`. You'll observe that after the first request, the server becomes unresponsive.

## Solution

The solution involves refactoring the code to use asynchronous operations instead of synchronous ones, allowing the event loop to continue processing other requests. The `bugSolution.js` file provides an example of how to do that using `async/await`.