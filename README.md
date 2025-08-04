# Week-1B_Q4
Below is documentation for the main functions in the provided C program for traversing a graph using Breadth-First Search (BFS), Depth-First Search (DFS), and Topological Sorting. This documentation assumes standard naming and arguments based on common practice and the function usage in your code.
Function Documentation
1. `buildGraph(struct Vertex **V)`
	•	Purpose: Constructs a graph based on user input by initializing vertices and edges.
	•	Parameters:
	•	`struct Vertex **V`: Pointer to the head pointer of the vertex list.
	•	Returns: void
	•	Usage: Call this at the start to input and build your graph’s structure.
2. `displayGraph(struct Vertex *V)`
	•	Purpose: Prints an adjacency list representation of the graph.
	•	Parameters:
	•	`struct Vertex *V`: Pointer to the head of the vertex list.
	•	Returns: void
	•	Usage: Prints out all vertices and their adjacent vertices in a user-friendly format.
3. `breadthFirstSearch(struct Vertex *V, int s)`
	•	Purpose: Traverses the graph using the Breadth-First Search (BFS) method starting from the source vertex `s`.
	•	Parameters:
	•	`struct Vertex *V`: Pointer to the head of the vertex list.
	•	`int s`: Index (0-based) of the source/start vertex for BFS.
	•	Returns: void
	•	Usage: Call after building the graph to perform BFS and process traversal-related information.
4. `printReachable(struct Vertex *V, int s)`
	•	Purpose: Prints all vertices that are reachable from the source vertex `s` using BFS results.
	•	Parameters:
	•	`struct Vertex *V`: Pointer to the head of the vertex list.
	•	`int s`: Index of the source vertex.
	•	Returns: void
	•	Usage: Should be called after `breadthFirstSearch()` to examine vertices that can be reached from the source.
5. `printShortestPath(struct Vertex *V, int src, int dst)`
	•	Purpose: Prints the shortest path from the source vertex `src` to the destination vertex `dst`.
	•	Parameters:
	•	`struct Vertex *V`: Pointer to the head of the vertex list.
	•	`int src`: Source vertex index.
	•	`int dst`: Destination vertex index.
	•	Returns: void
	•	Usage: Should be used after BFS traversal to extract shortest paths within the graph.
6. `depthFirstSearch(struct Vertex *V)`
	•	Purpose: Traverses the graph using Depth-First Search (DFS) from all unvisited vertices, marks cycles if found.
	•	Parameters:
	•	`struct Vertex *V`: Pointer to the head of the vertex list.
	•	Returns: void
	•	Usage: Initiates DFS traversal, updates global or external `cycle` variable if a cycle is found.
7. `topoSort(struct Vertex *V, struct listNode **Head)`
	•	Purpose: Performs Topological Sort of the graph and stores the result in a linked list.
	•	Parameters:
	•	`struct Vertex *V`: Pointer to the head of the vertex list.
	•	`struct listNode **Head`: Pointer to the head pointer of the list containing sorted vertices.
	•	Returns: void
	•	Usage: For directed acyclic graphs, sorts the vertices topologically.
8. `displayList(struct listNode *Head)`
	•	Purpose: Displays the contents of a linked list, typically used to show the result of a topological sort.
	•	Parameters:
	•	`struct listNode *Head`: Pointer to the head of the list.
	•	Returns: void
	•	Usage: Call after `topoSort()` to view the ordering.
9. `freeGraph(struct Vertex **V)`
	•	Purpose: Frees all memory allocated for the graph structure.
	•	Parameters:
	•	`struct Vertex **V`: Pointer to the head pointer of the vertex list.
	•	Returns: void
	•	Usage: Should be called at the end of the main program to prevent memory leaks.