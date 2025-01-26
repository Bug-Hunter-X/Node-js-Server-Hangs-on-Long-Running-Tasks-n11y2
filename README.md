# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js where a server can hang due to long-running operations blocking the event loop.  The `server.js` file shows the problematic code, while `server-solution.js` provides a solution using asynchronous operations.

## Problem

The original `server.js` contains a synchronous loop (`for` loop) within the request handler. This loop takes a significant amount of time to complete, blocking the event loop and preventing the server from responding to subsequent requests.  This leads to a hang or unresponsive server.

## Solution

The solution involves using asynchronous operations or offloading long-running tasks to other processes.  `server-solution.js` demonstrates this by using `setTimeout` to simulate an asynchronous operation.  For real-world applications, this might involve worker threads, child processes, or a message queue.