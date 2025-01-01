# PHP Undefined Index Notice from GET Parameter

This repository demonstrates a common PHP error: an undefined index notice resulting from accessing array elements using data from the GET request without proper error handling.  The `bug.php` file shows the problematic code, which crashes if a `id` parameter is missing from the URL.  The `bugSolution.php` file provides a corrected version with robust error handling.

## Problem

The original code lacks checks to see if the `id` parameter exists and if the corresponding array key exists within `$users`. Attempting to access a non-existent index results in a PHP warning: `Undefined index`. This can lead to unpredictable application behavior and security vulnerabilities.

## Solution

The solution introduces checks using `isset()` to validate both the GET parameter and array index before attempting to access data.  This prevents warnings and provides a more controlled and reliable way to handle missing or invalid input.  An appropriate message is also displayed to the user, instead of an error.

## How to run

1. Clone this repository.
2. Open `bug.php` and `bugSolution.php` in a PHP interpreter.
3. Access the scripts through your webserver (e.g., using `localhost/bug.php?id=1` or `localhost/bugSolution.php?id=1`)
4. Observe the difference in behavior when providing a valid or missing `id` parameter.