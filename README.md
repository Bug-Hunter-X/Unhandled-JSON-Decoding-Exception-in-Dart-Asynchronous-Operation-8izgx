# Unhandled JSON Decoding Exception in Dart

This repository demonstrates a common error in Dart when handling asynchronous operations that involve JSON decoding. The `fetchData` function fetches data from an API, decodes the JSON response, and prints a specific key. However, if the JSON response doesn't contain that key, a runtime exception occurs.

The `bug.dart` file contains the erroneous code, while `bugSolution.dart` provides a corrected version with robust error handling.

## How to Reproduce

1. Clone this repository.
2. Run `bug.dart`.  Observe that it crashes if the API response does not contain the expected key. 
3. Run `bugSolution.dart`. Observe improved error handling.

## Solution

The solution involves checking for the existence of the key before attempting to access it.  The improved code uses the `containsKey` method to gracefully handle the case where the key is missing.