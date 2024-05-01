# Algorithm
### Input:
Receive a vector of vectors pairs, where each inner vector represents a pair of integers.
### Initialization:
Create an unordered map g to store the adjacency list representation of the graph.
Create an unordered map deg to store the in-degree and out-degree of each node.
### Graph Construction:
Iterate through each pair p in pairs.
Add p[1] to the adjacency list of p[0] in g.
Increment the in-degree of p[1] and the out-degree of p[0] in deg.
### Find Source Node:
Define a lambda function getsrc to find the source node of the graph.
Iterate through each node e in deg.
If the difference between out-degree and in-degree is 1, set src to e.
If no such node is found, set src to any node e.
### Topological Sorting:
Initialize a deque path to store the topological order of nodes.
Initialize a stack st for DFS traversal.
Push src onto st.
While st is not empty:
Pop the top node u from st.
If the adjacency list of u is empty, push u to the front of path and pop u from st.
Otherwise, remove the first neighbor v of u from g[u] and push v onto st.
### Generate Result:
Initialize a vector of vectors ans to store the valid arrangement of nodes.
Calculate the size n of path.
Iterate from i = 0 to n - 2:
Push {path[i], path[i + 1]} to ans.
### Output: 
Return ans as the valid arrangement of nodes in topological order.
This algorithm performs a topological sort to find a valid arrangement of nodes in a directed graph based on the given pairs of edges.





