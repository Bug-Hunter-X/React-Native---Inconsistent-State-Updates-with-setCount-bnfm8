# React Native Inconsistent State Updates with setCount

This repository demonstrates a subtle bug in React Native related to state updates using `useState`. When `setCount` is called twice in rapid succession, the second call can overwrite the first, causing unexpected behavior.

## Bug Description
The issue arises when updating state multiple times within a single function call.  The asynchronous nature of state updates in React can lead to unexpected results if not handled properly.

## Solution
The solution involves using the functional form of `setCount`. This ensures that the update is always based on the most recent state value, preventing the overwrite issue. 

## How to reproduce
1. Clone this repository.
2. Run `npm install` or `yarn install` to install the dependencies.
3. Run the app on an emulator or physical device.
4. Observe that the counter increments inconsistently.