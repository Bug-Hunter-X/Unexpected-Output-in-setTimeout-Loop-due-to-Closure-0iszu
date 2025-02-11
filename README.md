# Unexpected Output in setTimeout Loop due to Closure

This repository demonstrates a common JavaScript error related to closures within `setTimeout` loops.  The issue arises when the loop's counter variable is not correctly captured within each callback function.

## The Problem

The `bug.js` file contains a function that uses `setTimeout` within a loop to print numbers 0-9 to the console after a delay. Due to closure issues, all callbacks will print the final value of `i` (which is 10). 

## The Solution

The `bugSolution.js` file provides a corrected version.  By using an Immediately Invoked Function Expression (IIFE), we create a new scope for each iteration, correctly capturing the value of `i`.