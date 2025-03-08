### Introduction to Graph Theory in Mathematics

Graph Theory is a branch of mathematics that studies graphs, which are mathematical structures used to model pairwise relations between objects. A graph consists of vertices (or nodes) and edges (or arcs) that connect these vertices. Vertices can represent various entities such as cities, people, or web pages, while edges can represent relationships like roads, friendships, or hyperlinks.

Graphs can be either directed or undirected. In an undirected graph, the edges have no direction; they simply connect two vertices. In a directed graph, each edge has a direction associated with it, indicating that one vertex points to another.

Graph Theory is widely used in various fields such as computer science (for network analysis), sociology (for studying social networks), biology (for modeling ecosystems), and more.

### Example of Graph Theory in Code

Let's consider a simple undirected graph with 4 vertices connected by 5 edges. We will represent this graph using an adjacency list, which is a common way to store graphs in computer science. An adjacency list uses a dictionary where each key is a vertex, and the corresponding value is a list of adjacent vertices.

Below is a Python code example demonstrating how to create such a graph and perform a basic operation, like printing all edges:

```python
# Define the graph as an adjacency list
graph = {
    'A': ['B', 'C'],
    'B': ['A', 'D'],
    'C': ['A', 'D', 'E'],
    'D': ['B', 'C', 'E'],
    'E': ['C', 'D']
}

# Function to print all edges in the graph
def print_edges(graph):
    edges = set()
    for vertex in graph:
        for neighbor in graph[vertex]:
            # To avoid duplicate edges, sort the tuple before adding it to the set
            edge = tuple(sorted((vertex, neighbor)))
            edges.add(edge)
    
    for edge in edges:
        print(f"Edge: {edge[0]} - {edge[1]}")

# Call the function to print all edges
print_edges(graph)

# Tags
#Graph Theory #Maths #python
```

In this code example, we define a graph with vertices 'A', 'B', 'C', 'D', and 'E'. We then create a function `print_edges` that prints each unique edge in the graph. The use of a set ensures that each edge is printed only once, even though they appear twice in the adjacency list representation (once for each vertex they connect).

#Graph Theory #Maths #python