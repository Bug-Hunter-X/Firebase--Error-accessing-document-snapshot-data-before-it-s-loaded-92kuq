# Firebase Asynchronous Data Access Error

This repository demonstrates a common error when using the Firebase SDK to access data from Firestore. The error occurs when trying to access a property of a document snapshot before the data has fully loaded.  The `bug.js` file contains code that reproduces the error, and `bugSolution.js` provides a solution.

## Problem
Accessing the `.data()` property of a `DocumentSnapshot` before the asynchronous operation completes results in undefined, causing the error `Cannot read properties of undefined (reading 'field')`.

## Solution
The solution involves using the `onSnapshot` listener's data parameter in conjunction with checking for null or undefined values before accessing properties.

## Setup
This assumes you've already set up a Firebase project and have the necessary configurations in place.