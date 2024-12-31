# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, this example shows a route that fetches a user by ID.  If the ID is not a valid integer, the application will likely crash or produce unexpected results.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides the corrected code.

## Bug

The bug lies in the lack of error handling when attempting to parse the user ID as an integer.  If the ID parameter is not an integer, `parseInt(userId)` will return `NaN`, causing the `find` method to fail silently or throw an error, depending on the surrounding code.