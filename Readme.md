# Python Labyrinth Solver with A* Algorithm

This Python script implements a labyrinth solver using the A* algorithm. The A* algorithm is a pathfinding algorithm that efficiently finds the shortest path between two points on a graph.

## Classes

### Labyrinth

- **Description**: Represents the labyrinth grid.
- **Attributes**:
  - `grid`: 2D array representing the labyrinth layout.
  - `size`: Size of the labyrinth grid (assuming it's a square).

### Node

- **Description**: Represents a node in the labyrinth grid.
- **Attributes**:
  - `x`: x-coordinate of the node.
  - `y`: y-coordinate of the node.
  - `g`: Cost of the path from the start node to this node.
  - `parent`: Parent node of this node in the path.
  - `h`: Heuristic estimate of the cost to reach the goal from this node.
- **Methods**:
  - `f()`: Calculates the total cost of the node.
  - `calculateH(goal)`: Calculates the heuristic estimate from this node to the goal.
  - `__str__()`: String representation of the node.
  - `__eq__(other)`: Equality check for nodes.

### Solver

- **Description**: Contains methods for solving the labyrinth.
- **Attributes**:
  - `labyrinth`: The labyrinth object to solve.
- **Methods**:
  - `get_successors(n)`: Gets the successor nodes for a given node.
  - `astar(start, end)`: Implements the A* algorithm to find the shortest path.
  - `showPath(finalNode)`: Prints the path from the start node to the final node.
