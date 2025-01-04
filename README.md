# Unresponsive Node.js Server: Synchronous Long-Running Task

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler can block the event loop, rendering the server unresponsive.

The `bug.js` file contains code that simulates a long-running task (5 seconds) within the request handler. This causes the server to hang and fail to respond to subsequent requests.

The `bugSolution.js` file presents a corrected version that uses asynchronous operations and prevents the event loop from being blocked.

## How to reproduce:

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js`
4. Open your browser and try to access `http://localhost:3000`. It will likely hang.
5. Now try running `node bugSolution.js` and repeat the steps.  It should respond much quicker.