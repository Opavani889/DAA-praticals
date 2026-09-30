Graph and Searching - DFS and BFS

Aim

To implement a graph and perform graph searching using Depth First Search (DFS) and Breadth First Search (BFS).

Description

A graph is a data structure consisting of vertices and edges.

This program represents an undirected graph using an adjacency matrix and performs two graph traversal techniques:

- Depth First Search (DFS)
- Breadth First Search (BFS)

DFS

Depth First Search explores a graph by going as deep as possible before backtracking.

DFS uses:

- Stack
- Recursion

In this program, DFS is implemented using recursion.

BFS

Breadth First Search visits vertices level by level.

BFS uses a queue.

Algorithm

DFS Algorithm

1. Start from the selected vertex.
2. Mark the vertex as visited.
3. Print the vertex.
4. Visit an unvisited adjacent vertex.
5. Repeat until all reachable vertices are visited.

BFS Algorithm

1. Start from the selected vertex.
2. Insert the vertex into a queue.
3. Mark it as visited.
4. Remove a vertex from the queue and print it.
5. Add its unvisited adjacent vertices to the queue.
6. Repeat until the queue becomes empty.

Example Graph

       0
      / \
     1   2
    / \   \
   3   4---+

Starting vertex = "0"

Example traversal:

DFS: 0 1 3 4 2
BFS: 0 1 2 3 4

Time Complexity

For an adjacency matrix:

- DFS: O(V²)
- BFS: O(V²)

where "V" is the number of vertices.

Space Complexity

- Graph adjacency matrix: O(V²)
- DFS/BFS additional space: O(V)

Language

C

File

"graph_dfs_bfs.c"