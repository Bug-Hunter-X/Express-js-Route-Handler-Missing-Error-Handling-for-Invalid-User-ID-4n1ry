# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the `/users/:id` route fails to handle cases where `:id` is not a valid number, potentially leading to application crashes or unexpected behavior.

The `bug.js` file shows the erroneous code. The `bugSolution.js` file provides a corrected version with proper error handling.

## How to reproduce the bug
1. Clone this repository.
2. Run `npm install express`
3. Run `node bug.js`
4. Send a GET request to `/users/abc` (or any non-numeric ID).  You'll likely see an error. 

## Solution
The solution involves adding input validation and error handling to gracefully manage invalid user IDs.