# Delivery Drone Path Planning

This project simulates a delivery drone navigating through a city environment using cell decomposition and the A* search algorithm. The goal is to find a safe and efficient route from a launch pad to a delivery destination while avoiding buildings and surrounding safety zones.

## Features

- 35 × 35 city grid
- A* pathfinding with 8-direction movement
- Euclidean-distance heuristic
- Building obstacles and safety buffers
- Prevention of diagonal corner-cutting
- Path smoothing for more natural drone movement
- Sparse, dense, narrow-passage, and blocked city scenarios
- Path-distance and explored-cell evaluation
- 2D map and interactive 3D visualization

## Technologies Used

- Python
- NumPy
- Matplotlib
- Plotly
- Jupyter Notebook

## How to Run

1. Download or open the notebook in Google Colab or Jupyter Notebook.
2. Run all cells in order.
3. Select a city type when prompted:
   - `1` — Sparse City
   - `2` — Dense City
   - `3` — Narrow Passage
   - `4` — Blocked Path
4. Review the generated route, performance results, and visualizations.

> The interactive 3D visualization may not appear directly on GitHub. Run the notebook in Google Colab or Jupyter Notebook to view it.

## Algorithm

The city is divided into grid cells, turning the navigation environment into a graph. The drone can move horizontally, vertically, or diagonally. A* uses the actual travel cost and a Euclidean-distance heuristic to find the shortest safe route.

After a path is found, line-of-sight smoothing removes unnecessary intermediate points to create a more natural flight path.

## Complexity

- Time complexity: `O(V log V)`
- Space complexity: `O(V)`

Here, `V` represents the number of cells in the grid.
