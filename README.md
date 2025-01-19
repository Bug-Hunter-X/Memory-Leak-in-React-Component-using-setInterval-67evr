# React setInterval Memory Leak
This repository demonstrates a common React bug involving memory leaks caused by the improper use of `setInterval` within the `useEffect` hook.

## The Problem
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second.  However, it lacks a cleanup function within the `useEffect` hook to stop the interval when the component unmounts. This results in the interval continuing to run indefinitely, even after the component is no longer rendered, leading to a memory leak.

## The Solution
The `bugSolution.js` file provides a corrected version of the component. It uses the return value of `useEffect` to define a cleanup function that calls `clearInterval` to stop the interval when the component is unmounted, preventing the memory leak.

## How to Run
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server.

You can then compare the behavior of the buggy and fixed components to see the difference.