# Genetic Algorithm for Solving the Traveling Salesman Problem (TSP)
This Python program implements a Genetic Algorithm (GA) to solve the **Traveling Salesman Problem (TSP)**. It evolves a population of possible routes between a set of cities to find the shortest possible route that visits each city exactly once and returns to the origin city.
## Dependencies
+ Python 3.x
+ NumPy
+ Matplotlib
```bash

pip install numpy matplotlib

```
## How to Run
Just run the script:

```python

python ga.py

```
It will:
+ Generate cities
+ Evolve the population over 10 generations
+ Print and plot the best route

## Features
+ Custom City, Route, and Population classes.
+ Genetic Algorithm with:
  + Tournament Selection
  + Order Crossover (OX)
  + Swap Mutation
  + Elitist Replacement
+ Fitness is inversely proportional to total path length.
+ Route visualizations using Matplotlib.
+ Annotated output with cost labels for each edge of the best path.

## How it works
1. **Cities Initialization**: Randomly generates 5 cities with (x, y) coordinates.
2. **Initial Population**: A set of random permutations (routes) of the cities.
3. **Evolution Process**:
   + **Selection**: Tournament selection of parents.
   + **Crossove**r: Combines parts of two parents to produce children.
   + **Mutation**: Randomly swaps two cities in a route.
   + **Replacement**: Replaces the old population with the new one.
4. **Visualization**: Plots the cities and draws arrows showing the shortest path found.

## Configuration
You can tweak these variables in the script:
``` python

popSize = 20              # Number of routes in the population
n_generations = 10        # Number of generations to evolve
tournament_size = 3       # Size of the tournament for selection
pc = 0.65                 # Crossover probability
pm = 0.1                  # Mutation probability

```
## Example output

## Notes
+ This version assumes exactly 5 cities. You can increase the number by modifying the loop that creates cities.
+ The crossover uses a fixed window of size 3.
