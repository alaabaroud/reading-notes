# Read: Graphs

A **Graph** is a non-linear data structure that consists of Nodes that can be called vertices that are connected with each other by edges.  


**Important terms: **
- Vertex: A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
- Edge:  An edge is a connection between two nodes.
- Neighbor: The neighbors of a node are its adjacent nodes, i.e., are connected via an edge. 
- Degree: The degree of a vertex is the number of edges connected to that vertex.

there are two main kinds of Graphs:

1- Undirected Graphs:
An undirected graph is a set of nodes and a set of links between the nodes. Each node is called a vertex, each link is called an edge, and each edge connects two vertices. The order of the two connected vertices is unimportant. An undirected graph is a finite set of vertices together with a finite set of edges.

![undirected](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3d/Undirected_graph.svg/1280px-Undirected_graph.svg.png)

2- Directed Graphs:

A directed graph, also called a digraph, is a graph in which the edges have a direction. This is usually indicated with an arrow on the edge. Unlike the Undirected graph, the digraph has arrows pointing to specific nodes.

![digraph](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a2/Directed.svg/1200px-Directed.svg.png)

**Notice the difference**
![graphs](https://sites.google.com/a/cs.christuniversity.in/discrete-mathematics-lectures/_/rsrc/1409480658489/graphs/directed-and-undirected-graph/dir.png)

-----------------------------------

**Complete vs Connected vs Disconnected**

- Complete Graphs:
A complete graph is when all nodes are connected to all other nodes.
- Connected:
A connected graph is graph that has all of vertices/nodes have at least one edge.
- Disconnected:
A disconnected graph is a graph where some vertices may not have edges.


**Acyclic vs Cyclic**

- Acyclic Graph:
An acyclic graph is a directed graph without cycles.

- Cyclic Graphs:
A Cyclic graph is a graph that has cycles.


