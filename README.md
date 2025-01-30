# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running operation in the request handler blocks the event loop, causing the server to become unresponsive.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The original `server.js` code includes a `while` loop that keeps the CPU busy for 5 seconds.  During this time, the event loop is blocked, and the server cannot handle any new requests.  This results in the server appearing to hang or become unresponsive to clients.