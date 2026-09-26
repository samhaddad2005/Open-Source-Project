# Open-Source-Project
This repository aims to act as a open source software that contains many graphing algorithms. Among said graphs, Dijkstra's algorithm — an algorithm that aims to solve the problem of finding the shortest paths between nodes in a graph. — is found under src/graphs_shaddad.

## Installation
```
pip install graphs_shaddad
```

## Dijkstra's Algorithm
The graph is a dictionary mapping each node to a dictionary of `{neighbor: weight}`.
```python
from graphs_shaddad.sp import dijkstra

graph = {
    0: {1: 4, 2: 8},
    1: {0: 4, 4: 6, 2: 3},
    2: {0: 8, 3: 2, 1: 3},
    3: {2: 2, 4: 10},
    4: {1: 6, 3: 10},
}
dist, path = dijkstra(graph, 0)
print(dist)  # {0: 0, 1: 4, 2: 7, 3: 9, 4: 10}
```


 <img width="400" height="324" alt="image" src="https://github.com/user-attachments/assets/82cb811e-dde9-4aed-b81e-7de8bbef569f" />


Explanation of the shortest paths:
- 0 -> 0 = 0: Source node itself, so distance is 0.
- 0 -> 1 = 4: Direct edge from node 0 to 1 gives shortest distance 4.
- 0 -> 2 = 7: Path 0 → 1 → 2 gives total cost 4 + 3 = 7, which is smaller than direct edge 8.
- 0 -> 3 = 9: Path 0 → 1 → 2 → 3 gives total cost 4 + 3 + 2 = 9.
- 0 -> 4 = 10: Path 0 → 1 → 4 gives total cost 4 + 6 = 10.

## Prim's Algorithm for Minimum Spanning Tree (MST)
```python
from graphs_shaddad.sp import Graph

g = Graph(5)
g.graph = [[0, 2, 0, 6, 0],
           [2, 0, 3, 8, 5],
           [0, 3, 0, 0, 7],
           [6, 8, 0, 0, 9],
           [0, 5, 7, 9, 0]]
g.primMST()  # prints each MST edge and its weight
```

Prim’s algorithm is a Greedy algorithm like Kruskal's algorithm. This algorithm always starts with a single node and moves through several adjacent nodes, in order to explore all of the connected edges along the way.

The algorithm starts with an empty spanning tree.
The idea is to maintain two sets of vertices. The first set contains the vertices already included in the MST, and the other set contains the vertices not yet included.
At every step, it considers all the edges that connect the two sets and picks the minimum weight edge from these edges. After picking the edge, it moves the other endpoint of the edge to the set containing MST. 
<img width="762" height="442" alt="image" src="https://github.com/user-attachments/assets/153ffc51-beac-4c83-bd24-c87062116569" />
