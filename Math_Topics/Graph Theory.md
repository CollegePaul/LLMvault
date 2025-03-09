### Introduction to Graph Theory

Graph theory is a branch of mathematics that studies graphs, which are mathematical structures used to model pairwise relations between objects. A graph in this context is made up of vertices (also called nodes) and edges, where each edge connects two vertices. 

Graphs can be either directed or undirected. In an undirected graph, the edges have no particular direction; they connect vertices bidirectionally. In a directed graph, also known as a digraph, the edges are ordered pairs of vertices, meaning that they point from one vertex to another in a specific direction.

#### Basic Concepts:
- **Vertices/Nodes**: The fundamental units within a graph.
- **Edges**: Connections between vertices. They can be weighted (having numerical values) or unweighted.
- **Degree of a Vertex**: In an undirected graph, the degree is the number of edges incident to it. In a directed graph, there is an in-degree (edges pointing towards the vertex) and an out-degree (edges pointing away from the vertex).
- **Path**: A sequence of vertices such that each adjacent pair of vertices is connected by an edge.
- **Cycle**: A path that starts and ends at the same vertex.
- **Connected Graph**: In an undirected graph, a graph is connected if there is a path between every pair of distinct vertices. For directed graphs, this concept can be extended to strongly connected (every vertex is reachable from every other vertex) and weakly connected (ignoring edge directions).
- **Complete Graph**: A simple graph in which every pair of distinct vertices is connected by a unique edge.

#### Example in Python:
Let's create a simple example using Python with the help of the `networkx` library, which is widely used for working with graphs.

```python
import networkx as nx
import matplotlib.pyplot as plt

# Create an undirected graph
G = nx.Graph()

# Add nodes
G.add_node(1)
G.add_nodes_from([2, 3, 4])

# Add edges
G.add_edge(1, 2)
G.add_edges_from([(1, 3), (2, 3), (3, 4)])

# Draw the graph
nx.draw(G, with_labels=True, node_color='lightblue', edge_color='gray')
plt.title("Simple Undirected Graph")
plt.show()

# Check if the graph is connected
print("Is the graph connected?", nx.is_connected(G)) # Output: Is the graph connected? True

# Degree of each vertex
degree_dict = dict(G.degree())
print("Degree of each vertex:", degree_dict) # Output: Degree of each vertex: {1: 2, 2: 2, 3: 3, 4: 1}
```

In this example, we created an undirected graph with four vertices and added several edges between them. We then checked if the graph is connected and printed the degree of each vertex.

#Graph Theory #Maths