
# Graph Search Algorithms and Minimax with Alpha-Beta Pruning

## Overview

This repository contains a set of search algorithms designed to traverse a graph, focusing on identifying the optimal path from a start node (`S`) to a goal node (`G`). Additionally, it covers the **Minimax** algorithm along with its improved version, **Alpha-Beta Pruning**.

### Graph Structure

The graph utilized in these algorithms is represented as follows:

```python
graph = {
    'S': {'A': 2, 'B': 3, 'C': 6},
    'A': {'D': 4, 'S': 2, 'B': 1},
    'B': {'A': 1, 'S': 3},
    'C': {'E': 5, 'S': 6},
    'D': {'A': 4, 'G': 3},
    'E': {'C': 5},
    'G': {'D': 3}
}
```

### Heuristic Values

Each node has a heuristic value, which is an estimate of the cost to reach the goal node `G`:

```python
heuristic = {
    'S': 7,
    'A': 5,
    'B': 4,
    'C': 6,
    'D': 2,
    'E': 4,
    'G': 0
}
```

## Search Algorithms

Below are the search algorithms implemented to find the best path from `S` to `G`:

1. **British Museum Search**: Explores all possible paths without considering optimization.
2. **Depth-First Search (DFS)**: Explores a path deeply before backtracking when needed.
3. **Breadth-First Search (BFS)**: Explores nodes level by level, moving to the next depth after exhausting the current one.
4. **Hill Climbing**: Selects the path with the lowest heuristic value at each step, without backtracking.
5. **Beam Search**: Limits the number of best paths explored at each level to a predefined number.
6. **Oracle Search**: Uses full knowledge of the graph to compute the shortest path directly.
7. **Branch and Bound (B&B)**: Evaluates paths but prunes paths that appear less promising based on cost.
8. **Branch and Bound Greedy**: Incorporates heuristic values to guide the search efficiently.
9. **Branch and Bound Greedy + Exit**: Exits immediately upon reaching the goal node.
10. **Branch and Bound Greedy + Heuristic**: Combines both cost and heuristic estimates in an aggressive manner.
11. **Branch and Bound with Heuristic**: Uses both path cost and heuristic estimates for node evaluation.
12. **A* Algorithm**: Combines path cost and heuristic to determine the optimal solution efficiently.

### Expected Results

For each algorithm, the expected output is:

```csharp
Best Path: ['S', 'A', 'D', 'G'] with cost 9
```

## Minimax Algorithm and Alpha-Beta Pruning

### Minimax Algorithm

The **Minimax Algorithm** is used to determine the best move in a two-player game. It works by evaluating possible future moves, with one player trying to maximize their score and the other trying to minimize it.

### Alpha-Beta Pruning

**Alpha-Beta Pruning** is an enhancement of the Minimax algorithm. It prunes unnecessary branches in the game tree, significantly improving efficiency without affecting the final result.

#### Key Concepts:

- **Maximizing Player**: Aims to maximize their score or benefit.
- **Minimizing Player**: Aims to minimize the maximizing player's score.
- **Alpha**: The highest value the maximizing player can achieve.
- **Beta**: The lowest value the minimizing player can achieve.

### Example Tree Structure

The following tree structure is used for both algorithms:

```
          N1
        /     \
      N2       N3
     /  \     /   \
   N4   N5  N6   N7
  / \   / \  / \   / \
 2   5 8   3 4   1 7   6
```

### Outputs

For both the Minimax algorithm and Alpha-Beta Pruning, the expected result is:

```arduino
Optimal value using Minimax: 6
Optimal value using Alpha-Beta Pruning: 6
```

Both algorithms arrive at the same optimal value, but Alpha-Beta Pruning performs the evaluation more efficiently by skipping redundant branches.
