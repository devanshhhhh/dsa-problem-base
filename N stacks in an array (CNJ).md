Link: https://www.codingninjas.com/studio/problems/n-stacks-in-an-array_1164271?leftPanelTab=1

Data structure design:
- `int* arr`: Points to the actual array that implements the stacks (size=s)
- `int* top`: Points to the array storing top elements of n stacks (size=n)
- `int *next`: Points to the array that stores next free index/next element's index in stack (going up) (size=s) 
- `int freespot`: Stores the next free index
- `int n`: Number of stacks 
- `int s`: Size of actual array

Ctor algo:
- Copy n and s from arguments
- Initialize arrays and assign pointers
- Assign 0 to the freespot
- Fill `top[]` with -1 (as there are no elements in any of the stack)
- Fill `next[]` with the next indices (next free index to that index), but make sure to explicitly assign -1 to last index of next (no next index exists)

Push(int x, int m) algo:
- Check if `freespot==-1`, if yes, return false (no space left)
- Else, continue and assign `int index=freespot`
- Update `freespot=next[index]`
- Assign `arr[index]=x`
- Update `next[index]=top[m-1]`
- Update `top[m-1]=arr[index]`

Pop(int m):
- Follow the push algo but in reverse, updating variable accordingly


#stack #hard #codingninjas 