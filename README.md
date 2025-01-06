# Unhandled Errors in Express.js Route Handler

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input or missing resources.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The original code attempts to fetch a user based on an ID passed in the URL. However, it fails to handle cases where:

1. The ID is not a valid number.
2. No user with the given ID exists.

These omissions can lead to unexpected behavior (e.g., crashes, cryptic error messages, or incorrect responses) in a production environment.

## Solution

The solution introduces robust error handling to address both scenarios.  It uses explicit checks and appropriate HTTP status codes to provide informative responses to the client.