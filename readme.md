# Dijkstra's Shortest Path Algorithm in Python

## Overview

This project implements **Dijkstra's Algorithm** in Python to find the shortest path from a source vertex to all other vertices in a weighted directed graph with non-negative edge weights.

The implementation uses a **Min-Heap (Priority Queue)** to efficiently select the next vertex with the minimum tentative distance.

---

## Features

- Finds the shortest distance from a source vertex to all other vertices.
- Reconstructs the shortest path for every destination.
- Uses a **Priority Queue (Min-Heap)** for improved performance.
- Displays both the shortest distance and the corresponding path.
- Easy to understand and modify for different graphs.

---

## Project Structure

```
.
├── dijkstra.py      # Python implementation
└── README.md        # Project documentation
```

---

## Requirements

- Python 3.x

No external libraries are required.

---

## How to Run

1. Clone the repository.

```bash
git clone https://github.com/your-username/dijkstra-algorithm.git
```

2. Navigate to the project directory.

```bash
cd dijkstra-algorithm
```

3. Run the program.

```bash
python dijkstra.py
```

---

## Graph Used

The graph is represented as an adjacency list.

```python
graph = {
    0: [(1, 4), (2, 1)],
    1: [(3, 1)],
    2: [(1, 2), (3, 5)],
    3: [(4, 3)],
    4: [(5, 2)],
    5: []
}
```

---

## Algorithm

### Dijkstra's Algorithm

1. Initialize all distances as infinity.
2. Set the source vertex distance to **0**.
3. Insert the source into a **Min-Heap**.
4. Repeatedly extract the vertex with the smallest distance.
5. Relax all adjacent edges.
6. Update distances and previous vertices whenever a shorter path is found.
7. Continue until all reachable vertices have been processed.

---

## Time Complexity

| Operation | Complexity |
|----------|------------|
| Overall | **O((V + E) log V)** |

Where:

- **V** = Number of vertices
- **E** = Number of edges

---

## Space Complexity

**O(V)**

Used for:

- Distance array
- Previous vertex array
- Priority queue
- Visited set

---

## Sample Output

```text
Shortest paths from vertex 0:

  Vertex   Distance                           Path
-------------------------------------------------------
       0          0                             0
       1          3                       0 -> 2 -> 1
       2          1                       0 -> 2
       3          4                  0 -> 2 -> 1 -> 3
       4          7             0 -> 2 -> 1 -> 3 -> 4
       5          9        0 -> 2 -> 1 -> 3 -> 4 -> 5
```

---

## Functions

### `dijkstra(graph, source)`

Computes the shortest distance from the source vertex to every other vertex.

**Parameters**

- `graph` – Adjacency list representation of the graph.
- `source` – Starting vertex.

**Returns**

- `dist` – List of shortest distances.
- `prev` – Previous vertex list for path reconstruction.

---

### `reconstruct_path(prev, source, target)`

Reconstructs the shortest path from the source to a target vertex.

**Parameters**

- `prev` – Previous vertex array.
- `source` – Starting vertex.
- `target` – Destination vertex.

**Returns**

- List representing the shortest path.

---

## Learning Objectives

- Understand Dijkstra's shortest path algorithm.
- Learn how a priority queue improves algorithm efficiency.
- Understand path reconstruction using the previous vertex array.
- Analyze the time and space complexity of graph algorithms.

---

## Author

**Kavi Priya**

---

## License

This project is intended for educational and learning purposes.

