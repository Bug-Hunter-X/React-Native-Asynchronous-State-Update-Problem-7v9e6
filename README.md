# React Native Asynchronous State Update Bug

This repository demonstrates a common bug in React Native applications: accessing state variables before the asynchronous `setState` call completes.  The `bug.js` file shows the problematic code, while `bugSolution.js` presents the corrected version.

## Problem

When fetching data asynchronously and updating state with `setState`, accessing the updated state immediately within the callback might lead to unexpected `null` values.  This is because `setState` is asynchronous; the state update doesn't happen instantaneously.  The solution is to use the updated state via the rendering lifecycle or callback functions provided by `setState`.