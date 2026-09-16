# Open-Source-Project
This repository aims to act as a open source software that contains many graphing algorithms. Among said graphs, Dijkstra's algorithm — an algorithm that aims to solve the problem of finding the shortest paths between nodes in a graph. — is found under src/graphs_shaddad.
```
cd src/graphs_shaddad
```
input: src = 0, adj[][] = [[[1, 4], [2, 8]], [[0, 4], [4, 6], [2,3]], [[0, 8], [3, 2], [1,3]], [[2, 2], [4, 10]], [[1, 6], [3, 10]]]


 <img width="400" height="324" alt="image" src="https://github.com/user-attachments/assets/82cb811e-dde9-4aed-b81e-7de8bbef569f" />


Output:  [0, 4, 7, 9, 10]
Explanation:  Shortest Paths:  
0 -> 0 = 0: Source node itself, so distance is 0.
0 -> 1 = 4: Direct edge from node 0 to 1 gives shortest distance 4.
0 -> 2 = 7: Path 0 → 1 → 2 gives total cost 4 + 3 = 7, which is smaller than direct edge 8.
0 -> 3 = 9: Path 0 → 1 → 2 → 3 gives total cost 4 + 3 + 2 = 9.
0 -> 4 = 10: Path 0 → 1 → 4 gives total cost 4 + 6 = 10.
