# COBOL Looping Error: Unexpected Termination

This repository demonstrates a common error in COBOL programs related to loop termination conditions. The program intends to display numbers from 1 to 10, but it may end prematurely or unexpectedly due to an error in the loop's UNTIL condition.

## Bug Description
The `UNTIL` condition in the `PERFORM VARYING` statement might cause the loop to terminate sooner than expected. This can happen because of an incorrect comparison or other logic issues within the condition.   The provided `bug.cob` file contains this potential error. The `bugSolution.cob` provides a correction of this problem.

## How to Reproduce
1. Compile and run `bug.cob`.
2. Observe the output. It may not display all numbers from 1 to 10. 
3. Compile and run `bugSolution.cob` to see the expected output.

## Solution
The solution involves carefully checking and ensuring that the loop's termination condition is correctly set up to cover all expected iterations. The correct condition should be `UNTIL WS-COUNTER > 10`. This ensures the loop executes for numbers 1 through 10.