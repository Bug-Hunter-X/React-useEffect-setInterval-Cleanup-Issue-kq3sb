# React useEffect setInterval Cleanup Issue
This repository demonstrates a common error in React applications: the improper use of `setInterval` within the `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior in your application.

## Problem
The `setInterval` function, when used within `useEffect` without a cleanup function, continues to run even after the component unmounts. This causes the counter to keep incrementing in the background, leading to potential memory leaks and unexpected behavior.

## Solution
To fix this, you must use the return value of `useEffect` to add a cleanup function that clears the interval before unmounting. This ensures that the interval stops running as expected.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the counter incrementing even when the component is unmounted (you will have to refresh or navigate away from the page and back to verify this).