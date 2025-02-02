# React setInterval Memory Leak
This repository demonstrates a common React bug involving memory leaks caused by improper usage of `setInterval` within the `useEffect` hook.  The `bug.js` file shows the faulty code, while `bugSolution.js` provides the corrected implementation.

## Problem
The original code uses `setInterval` to update a counter every second.  However, it fails to include a cleanup function in the `useEffect` hook's return statement.  This results in a memory leak because the interval continues to run even after the component unmounts.

## Solution
The corrected code includes a cleanup function that uses `clearInterval` to stop the interval when the component unmounts. This prevents the memory leak.

## How to Run
1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run `npm install` to install necessary dependencies.
4. Run `npm start` to start the development server.