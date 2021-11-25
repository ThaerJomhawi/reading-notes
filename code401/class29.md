# Graphs

A graph is a non-linear data structure that can be looked at as a collection of `vertices` (or nodes) potentially connected by line segments named `edges`.

1. **Vetex**: is a data object that can have zero or more adjacent vertices.
2. **Edge**: is a connection between two nodes.
3. **Neighbor**: The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
4. **Degree**: The degree of a vertex is the number of edges connected to that vertex.

**[Undirected Graphs]**

that the undirected graph does not move in any direction.

**[Directed Graphs (Digraph)]**

Each node is directed at another node with a specific requirement of what node should be referenced next.

### Complete vs Connected vs Disconnected

1. **Complete Graphs**
   A complete graph is when all nodes are connected to all other nodes.

2. **Connected**
   A connected graph is graph that has all of vertices/nodes have at least one edge.

3. **Disconnected**
   A disconnected graph is a graph where some vertices may not have edges.

### Acyclic vs Cyclic

**[Acyclic Graph]**

A cycle is when a node can be traversed through and potentially end up back at itself.

**[Cyclic Graphs]**

A cycle is defined as a path of a positive length that starts and ends at the same vertex.

### Graph Representation

- **Adjacency Matrix**
  An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix



a **sparse graph** is when there are very few connections. a **dense graph** is when there are many connections

> **Within an adjacency matrix, an undirected graph will always be symmetric. This is not the case for a directed graph.**

- **Adjacency List**

An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.



> **we can see that we will only place the vertices that are connected in the list. If there is no connection between the vertices, they are not listed.**

### Weighted Graphs

A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights.