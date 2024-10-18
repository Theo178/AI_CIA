# Let's create the markdown file with the provided content and make it downloadable.

# Content of the markdown file
md_content = """
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
