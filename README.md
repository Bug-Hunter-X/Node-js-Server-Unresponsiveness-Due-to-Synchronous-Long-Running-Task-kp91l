# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler causes the server to become unresponsive.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations and promises.

## Bug Description

The server hangs because the `while` loop in the request handler keeps the event loop busy for 5 seconds, preventing any other requests from being processed during that time.  This can lead to poor performance and unresponsiveness.

## Solution

The solution utilizes asynchronous programming techniques to avoid blocking the event loop.  This ensures that other requests can be processed concurrently without causing the server to hang.