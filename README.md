# spanning-tree-finder
Implements Breadth-First-Search and Depth-First-Search to find Spanning Trees in a graph.  

## What is
A spanning tree of a connected graph G is a subgraph of G that contains all the vertices in G and is a tree.  
A tree is an undirected graph that is connected and has no cycles.  

Breadth-First Search (BFS) and Depth-First Search (DFS) start at a single vertex and incrementally build a connected tree
by adding edges and vertices.  The resulting tree is rooted at the start vertex.  

DFS goes deep into the graph and produces trees with longer paths from the start vertex.  
BFS explores graph by distance from initial vertex, starting with neighbors and expanding to neighbors of neighbors.  

## Pseudocode
### DFS
G is undirected, connected Graph
T is spanning tree (Vertexes, Edges)

visit(v)  
For every neighbor w of v  
  * if w not in T  
    * add w to T  
    * add {v,w} to T  
    * visit(w)  

### BFS
G is undirected, connected graph
T is spanning tree
neighbors are visited in ascending ASCII order of name

Add v1 to T
Add v1 to back of list (queue)

While the list is not empty:
 * remove vertex v from the front of the list (queue)
 * For each neighbor w of v that is not already in T:
   * Add w and {w,v} to T
   * Insert w at the back of the list


