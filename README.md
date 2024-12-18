# Unhandled Promise Rejection in Express.js Async Middleware

This repository demonstrates a common error in Express.js applications:  unhandled promise rejections within asynchronous middleware.  The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a corrected version with comprehensive error handling.

## Problem

The original code uses a `Promise` within a route handler but lacks proper `.catch()` handling for potential errors. This can lead to server crashes or unexpected behavior without any indication of the underlying issue.

## Solution

The solution demonstrates how to robustly handle these errors.  It uses a centralized error handler to gracefully manage errors and provide appropriate responses to the client.  Using a global error handler ensures that all unhandled errors are caught, improving application stability and providing better user experience.