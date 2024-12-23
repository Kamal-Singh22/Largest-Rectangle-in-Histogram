# Largest-Rectangle-in-Histogram
Given an array of integers heights representing the heights of bars in a histogram, find the area of the largest rectangle that can be formed in the histogram.
Explanation:
Stack-Based Approach:

The stack stores indices of the heights array in increasing order of height.
When a bar of smaller height is encountered, the area of the rectangle formed with the bar at the top of the stack as the smallest bar is calculated.
Key Operations:

Push indices onto the stack if the current height is greater than or equal to the height of the top of the stack.
Pop from the stack if the current height is less, and calculate the area using:
width = currentIndex - stack.peek() - 1 (if stack is not empty)
width = currentIndex (if stack is empty)
Edge Case:

Append a height of 0 at the end to ensure all bars are processed.
