Link: https://leetcode.com/problems/group-anagrams

Approach-1:
- Use a `map<string, vector<strings>>` to create groups
- Use the sorted version of current string to be `map.first` and insert all strings that give the same sorted string in the corresponding mapped vector
- Once, groups are made, run a for loop on the map and insert these groups in the answer vector
- Return the ans
- TC: **O(nk log k)**
- SC: **O(nk)**

Approach-2:
- To save the time to sort, use a hash array as your key instead of sorted string as key
- Declare a hasher function 
- Modify the map to be `map<array<int, 256>, vector<strings>>`
- And mapping as `mp[hasher(str)].push_back(str)`
- TC: **O(nk)**
- SC: **O(nk)**

***Realistically approach-1 is more efficient***

#strings #hard #leetcode 