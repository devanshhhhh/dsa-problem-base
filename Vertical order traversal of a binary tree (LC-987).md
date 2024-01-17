Link: https://leetcode.com/problems/vertical-order-traversal-of-a-binary-tree/ 

Approach:
- Use a `map<int, vector<pair<int, int>>> mp` to store `<breadth: <corresponding element, height>>`
- Write a recursive function to populate the map
- Now write a custom comparator that sort all the vectors by `height` (if same height, pick greater value)
- Iterate over the map and pick vector corresponding to each `breadth`, sort the vector by height using STL sort and your custom comparator
- Once done, insert first values from your pairs in that vector to a vector and push it to your solution vector
- Return your solution vector

//This can also be done using a multiset and queue but this feels more intuitive and efficient (imo)

#trees #leetcode #hard 