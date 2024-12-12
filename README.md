# React useEffect setInterval memory leak

This repository demonstrates a common error in React applications: memory leaks caused by improper usage of `setInterval` within the `useEffect` hook.

## The Problem

The `bug.js` file contains a React component that uses `setInterval` to update a count every second.  However, the cleanup function within the `useEffect` hook is incorrect, leading to multiple intervals running concurrently, consuming excessive memory and causing performance issues.  

## The Solution

The `bugSolution.js` file provides a corrected version, ensuring that only one interval is running at any given time, properly cleaning up the interval when the component unmounts or the effect runs again.  This prevents the memory leak.