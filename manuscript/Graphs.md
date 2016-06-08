# Graphs

The structure presented in the previous chapter is called a [_graph_][graph]. A
graph is a collection of objects called _vertices_ and there connections called
_edges_. Graphs are ubiquitous. The world wide web can be seen as a graphs as
well as social networks.

Graphs have various different representations. The table that listed the states
that could be reached from a given state of the wolf, sheep and cabbage puzzle
is one, and is called _adjacency list_. It tells you if two vertices are
neighbors. 

Two others could be the _adjacency matrix_ and the _incidence matrix_.

## Adjacency matrix
An adjacency matrix is a matrix where the rows and columns are the vertices. The
matrix has a zero if the corresponding vertices are not connected by an edge,
and has a one if the corresponding vertices are connected by an edge.

## Incidency matrix
An incidency matrix has as rows the vertices of a graph and as columns the
edges. It has ones for every edge that a vertex is incident with.

## Excercises

1. Create an adjacency matrix for the wolf, sheep and cabbage graph.
2. Create an incidence matrix for the wolf, sheep and cabbage graph.

## Implementation
Create a representation of a graph in code and use it to represent the wolf,
sheep and cabbage graph.
 
[graph]: https://en.wikipedia.org/wiki/Graph_(discrete_mathematics)
