Approach:
- Take a stack and push -1 as the last element would have no element smaller going forward
- Start the traversal from the last element
- If you find a smaller element on top of stack, store it as answer for the corresponding index and push your current number to stack
- Move back and do the same
- If the top is greater, pop until you find a smaller number (would always be true since -1 is at bottom)
- TC: **O(n)**
- SC: **O(n)**

#stack #self 