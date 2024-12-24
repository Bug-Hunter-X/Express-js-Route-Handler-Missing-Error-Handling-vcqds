# Express.js Route Handler Missing Error Handling

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  The example shows a route that fetches a user by ID.  If the ID is invalid (e.g., not a number, or not found), the application crashes or returns unexpected results.

The solution demonstrates proper error handling by validating the ID and returning an appropriate HTTP status code if an error occurs. 

## Bug

The `bug.js` file contains the erroneous code.  It attempts to parse the user ID as an integer but doesn't handle the case where the ID is not a valid integer or when no user with the matching ID exists.

## Solution

The `bugSolution.js` file provides a corrected implementation. It includes error handling to check for invalid input and returns an appropriate HTTP response (400 Bad Request or 404 Not Found) if the user ID is invalid or the user is not found.  This ensures a more robust and user-friendly experience. 