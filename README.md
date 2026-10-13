# PBLE 2: Campus Shortest Route Finder – Dijkstra's Algorithm

## 1. Project Overview

The **Campus Shortest Route Finder** is a menu-driven C program that finds the shortest distance between a selected source location and all other locations on a college campus using Dijkstra's Algorithm.

The campus is represented as a weighted graph using an adjacency matrix, where locations are vertices and roads are edges with associated distances.

## 2. Objectives

- Represent a weighted graph using an adjacency matrix.
- Implement Dijkstra's Shortest Path Algorithm.
- Calculate the shortest distance from a selected source to all other locations.
- Display the shortest path to each reachable destination.
- Understand the greedy method and time complexity of the algorithm.

## 3. Technologies Used

- **Programming Language:** C
- **Concepts:** Weighted Graph, Greedy Method, Dijkstra's Algorithm, Adjacency Matrix
- **Data Structures:** Arrays
- **Compiler:** GCC or any standard C compiler

## 4. Features

- Menu-driven interface that continues until the user selects Exit.
- Enter campus locations and road distances.
- Display the adjacency matrix.
- Select a source location.
- Calculate shortest distances using Dijkstra's Algorithm.
- Display shortest paths using a parent array.
- Identify unreachable locations.
- Handle invalid menu choices and invalid distance values.

## 5. Sample Campus Locations

1. Main Gate
2. Library
3. Computer Department
4. Laboratory
5. Auditorium

Users can also enter their own campus locations and road distances.

## 6. Menu Options

1. Enter Campus Graph
2. Display Adjacency Matrix
3. Select Source Location
4. Find Shortest Distance
5. Display Shortest Paths
6. Display Distance from Source to All Locations
7. Exit

## 7. Algorithm

1. Initialize the source distance to `0` and all other distances to `INF`.
2. Initialize all vertices as unvisited and all parent values to `-1`.
3. Select the unvisited vertex with the minimum distance.
4. Mark the selected vertex as visited.
5. Update the distances of its adjacent vertices if a shorter path is found.
6. Store the predecessor of each updated vertex in the parent array.
7. Repeat until all reachable vertices have been processed.
8. Display the shortest distances and reconstruct the paths using the parent array.

## 8. Sample Output

**Source:** Main Gate

| Destination | Shortest Distance | Shortest Path |
|---|---:|---|
| Library | 4 | Main Gate → Library |
| Computer Department | 7 | Main Gate → Library → Computer Department |
| Laboratory | 9 | Main Gate → Library → Computer Department → Laboratory |
| Auditorium | 12 | Main Gate → Library → Computer Department → Laboratory → Auditorium |

*The above output corresponds to the sample road network used for testing.*

## 9. Time Complexity

**Time Complexity: O(V²)**

The algorithm selects the minimum-distance unvisited vertex by scanning all vertices and checks adjacent vertices using the adjacency matrix. These operations take O(V) time per vertex and are repeated up to V times.

**Space Complexity: O(V²)**

The adjacency matrix requires O(V²) space, while the distance, visited, and parent arrays require O(V) additional space.

Here, V represents the number of campus locations (vertices).

## 10. Limitations and Assumptions

- All road distances must be non-negative.
- The campus road network is treated as an undirected graph.
- A distance of `0` between different locations indicates that no direct road exists.
- The program uses a fixed maximum capacity of 20 locations.
- `INF` represents the absence of a direct connection or an unreachable destination.

## 11. How to Compile and Run

Save the source code as `campus_shortest_route.c`.

Compile using GCC:

```bash
gcc campus_shortest_route.c -o campus_shortest_route
```

Run on Linux or macOS:

```bash
./campus_shortest_route
```

On Windows:

```bash
campus_shortest_route.exe
```

## 12. Conclusion

This project demonstrates the practical application of Dijkstra's Algorithm for finding the shortest routes in a weighted graph. It helps understand graph representation, the greedy approach, distance updates, predecessor arrays, path reconstruction, and complexity analysis.

The program can be used as a basic campus navigation system to calculate the shortest distances from a selected location to other campus locations.
