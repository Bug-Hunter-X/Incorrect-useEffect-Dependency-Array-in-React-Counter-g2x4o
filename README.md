# Incorrect useEffect Dependency Array in React Counter
This repository demonstrates a common bug in React applications involving the `useEffect` hook and its dependency array. The provided code implements a simple counter that updates every second. However, due to an incorrect dependency array, the counter does not update as expected.

## Bug Description:
The `useEffect` hook is used to set up a timer that increments a counter every second. The dependency array is empty (`[]`), which means the effect only runs once after the component mounts.  Because 'count' is not included in the dependency array, the effect does not re-run when the 'count' value changes, resulting in a broken counter.

## Solution:
The solution is to include the `count` variable in the dependency array. This ensures that the effect re-runs whenever the `count` value changes.