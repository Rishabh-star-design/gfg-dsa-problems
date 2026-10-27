## 01. Graph Adjacency List Traversal

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/print-adjacency-list-1587115620/1)

### Problem Description

**Task:** Given an undirected graph with V nodes and E edges, create and return an adjacency list of the graph. 0-based indexing is followed everywhere.Example 1:Input:V = 5, E = 7edges = [[0,1], [0,4], [4,1], [4,3], [1,3], [1,2], [3,2]]

#### Examples

##### Example 1

- **Explanation:** Node 0 is connected to 2 and 3.Node 1 is only connected to 2.Node 2 is connected to 0 and 1.Node 3 is only connected to 0.Constraints:1 ≤ V, E ≤ 10⁵

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(V + E)
- **Expected Auxiliary Space Complexity:** O(V + E)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-10-27 20:47:19
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    vector<vector<int>> printGraph(int V, vector<pair<int, int>>& edges) {
        
        vector<vector<int>> adj(V);//adj list tayar hai
        for(auto &e :edges){
            int u=e.first;
            int v=e.second;
            
            //dono tarf ki edge ko print krna hoga bc remember
            adj[u].push_back(v);
            adj[v].push_back(u);
        }
        
        return adj;
    }
};
```

*Generated on: 10/27/2026, 8:54:45 PM*