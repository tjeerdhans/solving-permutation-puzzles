# Dijkstra Shortest Path Algorithm

We have learned that using a graph can help in solving a puzzle. But if the
graphs gets larger, visual inspection could get unwieldy. Furthermore, a
computer can not rely on visual inspection any time soon and should use an other
representation.

| State  | Neighbors     |
|------------------------|
| 1  | 5, 9, 10, 11      |
| 2  | 13, 14            |
| 3  | 10, 13, 15        |
| 4  | 14, 15            |
| 5  | 1                 |
| 6  | 16                |
| 7  | 14, 16            |
| 8  | 16                |
| 9  | 1                 |
| 10 | 1, 3              |
| 11 | 1                 |
| 12 | 16                |
| 13 | 2, 3              |
| 14 | 2, 4, 7           |
| 15 | 3, 4              |
| 16 | 6, 7, 8, 12       |

With the representation above, how could one find a path from a vertex 1 to
vertex 16? One way is to use [Dijkstra shortest path algorithm][dijkstra].

Dijkstra shortest path algorithm has some great properties

1. If there is a path is will find it.
2. The path that is returned by the algorithm is the shortest.
3. It is fairly efficient in finding the shortest path.

Note that it could be the case that the shortest path is not unique, i.e. that
there are multiple different path of the same length. Dijkstra shortest path
algorithm will still find a path.

## Pseudo Code

We will now proceed to describe the algorithm in pseudo code. The algorithm
accepts as its arguments a graph `G`, a `start` vertex of the graph and a `finish`
vertex. It will return a shortest path from `start` to `finish`.

The algorithm maintains for each vertex of the graph a shortest path that from
`start` to the particular vertex. To start, we initialize every path as though
it is unreachable, except for that `start` vertex.

We also maintain a queue of vertices that we need to visit. We initialize with
the `start` vertex.

Now we loop over the queue of vertices we need to visit until either it is empty
or we reach the `finish` vertex. Take the vertex with the shortest path of the
queue. For each neighbor update the known paths and add the neighbors that we
encounter for the first time.

## Exercises
Use Dijkstra shortest path algorithm to solve the wolf, sheep and cabbage
puzzle.

## Implementation
1. Implement Dijkstra shortest path algorithm
2. Use it to solve the Wolf, Sheep and Cabbage puzzle

[dijkstra]: https://en.wikipedia.org/wiki/Dijkstra's_algorithm

