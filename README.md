# Express.js JSON Body Parsing Issue

This repository demonstrates a common issue encountered when using Express.js to parse JSON request bodies: failure to handle empty or invalid JSON data.  The `express.json()` middleware expects well-formed JSON.  If the request body is empty or contains malformed JSON, it will throw an error or simply not parse the body correctly, leading to unexpected behavior.

The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution that handles these cases gracefully.

## Bug

The provided `bug.js` showcases an Express.js server that attempts to parse a JSON request body. However, if the request body is empty or contains malformed JSON, the server fails to handle it properly, potentially leading to server errors or unexpected results.

## Solution

The `bugSolution.js` file demonstrates a more robust solution. It checks if `req.body` is empty or contains errors before accessing its properties, preventing unexpected crashes or incorrect data processing.