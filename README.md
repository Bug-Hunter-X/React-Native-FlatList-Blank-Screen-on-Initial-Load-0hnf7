# React Native FlatList Blank Screen on Initial Load

This repository demonstrates a common issue in React Native where a FlatList component renders a blank screen on the initial load, even after data is successfully fetched.  The problem stems from the component rendering before the data is available in the state.

## Bug

The `bug.js` file shows the initial implementation with the problem.  The FlatList is rendered before the `useEffect` hook finishes fetching the data. The app will first show a blank screen before showing the data after 2 seconds.

## Solution

The `bugSolution.js` file shows the solution by introducing a loading state to conditionally render content while the data is being fetched, solving the blank screen issue.

## How to reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `npx react-native run-android` or `npx react-native run-ios`.

Observe the initial blank screen before the data appears.

## Steps to solve

1. Add a loading state variable.
2. Conditionally render the FlatList only when the data is available and loading is false.
3. Display a loading indicator while the data is fetched.