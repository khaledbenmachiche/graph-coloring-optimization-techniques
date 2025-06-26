# Graph Coloring Algorithms
This repository contains a comprehensive collection of algorithms for solving the graph coloring problem, ranging from exact methods to various heuristic approaches.

## Introduction

The graph coloring problem is a classic NP-hard problem in computational complexity theory. The goal is to assign colors to the vertices of a graph such that no two adjacent vertices share the same color, while minimizing the total number of colors used.

This problem has numerous applications including:
- Scheduling and timetabling
- Register allocation in compilers
- Frequency assignment in radio networks
- Map coloring
- Pattern matching
- Sudoku solving

## Implementation

This repository implements the following algorithms categorized by their approach:

### Exact Methods

- **Branch and Bound**: Systematically explores the search space with pruning to find the optimal solution
- **Dynamic Programming**: Solves overlapping subproblems to build up the optimal solution

### Constructive Heuristics

- **Greedy Coloring**: Sequential vertex coloring with various ordering strategies
- **DSatur (Degree of Saturation)**: Colors vertices based on their saturation degree
- **RLF (Recursive Largest First)**: Recursively colors maximal independent sets
- **Welsh-Powell Algorithm**: Colors vertices in decreasing order of degree

### Meta-heuristics

- **Simulated Annealing**: Uses temperature-based probabilistic acceptance criteria to escape local optima
- **Tabu Search**: Employs memory structures to guide the search through the solution space
- **Genetic Algorithms**: Evolves a population of colorings using selection, crossover, and mutation
- **Ant Colony Optimization**: Mimics the behavior of ants to find good colorings


## Benchmark Graphs

The repository includes standard benchmark graph instances from:
- DIMACS Graph Coloring Challenge
- COLOR02/03/04 Instances
- Random graphs with various densities
- Real-world application graphs

## Performance Comparison

We provide comprehensive performance metrics including:
- Color count (solution quality)
- Computation time
- Memory usage
- Convergence behavior for iterative methods
- Scalability analysis
- Statistical performance across multiple runs

## Getting Started

### Prerequisites
- Python 3.8+
- Required packages: numpy, scipy, matplotlib, networkx, pulp

### Installation

```bash
# Clone the repository
git clone https://github.com/khaledbenmachiche/GraphColoringProblem.git

# Navigate to the directory
cd GraphColoringProblem

# Install requirements
pip install -r requirements.txt
```

## Project Structure

```
GraphColoringProblem/
├── notebooks/                     # Jupyter notebooks containing algorithm implementations
│   ├── exact_methods.ipynb        # Implementation of exact coloring algorithms
│   ├── heuristics.ipynb           # Implementation of heuristic approaches
│   ├── local_search.ipynb         # Local search methods and metaheuristics
│   ├── genetic.ipynb              # Genetic algorithm implementation
│   └── ant_colony_optimisation.ipynb  # Ant Colony Optimization algorithm
├── data/                          # Benchmark graph instances
│   ├── dsjc250.5.col              # DIMACS format graph instance
│   ├── dsjc500.9.col              # DIMACS format graph instance
│   ├── dsjr500.1c.col             # DIMACS format graph instance
│   ├── flat1000_76_0.col          # DIMACS format graph instance
│   └── r250.5.col                 # DIMACS format graph instance
├── README.md                      # Project documentation
├── requirements.txt               # Required Python packages
```

## References

- [Graph Coloring Problem Overview](https://en.wikipedia.org/wiki/Graph_coloring)
- Lewis, R. (2015). A Guide to Graph Colouring: Algorithms and Applications. Springer.
- Galinier, P., & Hao, J. K. (1999). Hybrid evolutionary algorithms for graph coloring. Journal of Combinatorial Optimization, 3(4), 379-397.
- Brélaz, D. (1979). New methods to color the vertices of a graph. Communications of the ACM, 22(4), 251-256.
- Burke, E. K., et al. (2013). Hyper-heuristics: a survey of the state of the art. Journal of the Operational Research Society, 64(12), 1695-1724.
