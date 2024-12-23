# Expo Camera Initialization Race Condition

This repository demonstrates a common error when using the Expo Camera API: attempting to access camera features before the camera is fully initialized.  This can lead to unpredictable behavior or crashes.

The `bug.js` file shows the problematic code, where camera properties are accessed too early, potentially before initialization is complete. The `bugSolution.js` file presents a solution to handle this issue gracefully.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `expo start` to start the Expo development server.
4. Observe the error on the device/simulator.
5. Compare the behavior with `bugSolution.js` to see the correct implementation.

## Solution

The solution uses a state variable to track the camera's readiness and prevents accessing camera features until it's confirmed to be initialized.