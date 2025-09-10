---
title: An Exploration of Perlin Noise Terrain Generation and Pathfinding
date: 2025-09-10
image: assets/images/posts/visualizing-terrain/mesh-terrain.png
blurb: This project was created as a demonstration and learning exercise to explore procedural terrain generation, pathfinding algorithms, and advanced data visualization in Python. It is designed to help understand and communicate key concepts in algorithmic problem solving, spatial data processing, and scientific visualization...
---

# Demonstration & Learning Project: Procedural Terrain Generation & Pathfinding Visualization

## Overview
This project was created as a demonstration and learning exercise to explore procedural terrain generation, pathfinding algorithms, and advanced data visualization in Python. It is designed to help understand and communicate key concepts in algorithmic problem solving, spatial data processing, and scientific visualization. The notebook is interactive, educational, and visually engaging—ideal for both personal learning and sharing with others.

---

## Features
- **Procedural Terrain Generation**: Uses Perlin noise and Gaussian filtering to create realistic, high-resolution terrain.
- **A* Pathfinding**: Implements modular A* with 8-directional movement, supporting multiple waypoints.
- **2D & 3D Visualization**:
  - 2D contour plots with start, end, and intermediary waypoints.
  - 3D surface plots for terrain elevation.
  - Animated pathfinding visualization.
  - Interactive 3D mesh with pythreejs, including overlays for waypoints and the computed path.
- **Clean, Modular Code**: Well-commented, organized, and easy to extend.

---


## Technologies Used
- Python (NumPy, Matplotlib, SciPy, noise, heapq)
- pythreejs (for interactive 3D visualization)

---

## Key Code Highlights
### 1. Terrain Generation
- Generates a 2D array using Perlin noise, then applies normalization and Gaussian smoothing for realistic elevation.
- Example:
  ```python
  terrain = np.zeros((height, width))
  for y in range(height):
      for x in range(width):
          value = noise.pnoise2(x * scale, y * scale, octaves=octaves, persistence=persistence)
          terrain[y][x] = value
  terrain = (terrain + 1) / 2
  terrain = terrain ** 2
  terrain = terrain * 900 + 100
  terrain = scipy.ndimage.gaussian_filter(terrain, filter_size)
  ```
# ![Terrain Generation](/assets/images/posts/visualizing-terrain/3d-terrain.png)

### 2. Modular A* Pathfinding
- Finds the shortest path through multiple waypoints using 8-directional movement and elevation-aware cost.
- Example:
  ```python
  def astar_8dir(terrain, start, end):
      # ...existing code...
      return path
  waypoints = [start, intermediary_one, intermediary_two, end]
  full_path = []
  for i in range(len(waypoints) - 1):
      segment = astar_8dir(terrain, waypoints[i], waypoints[i+1])
      # ...existing code...
  ```
# ![Terrain Waypoints](/assets/images/posts/visualizing-terrain/2d-terrain-with-plots.png)

### 3. Visualization
- 2D contour and 3D surface plots using Matplotlib.
- Animated pathfinding using FuncAnimation.
- Interactive 3D mesh with pythreejs, including colored terrain, markers, and path overlays.
# ![Terrain Waypoints](/assets/images/posts/visualizing-terrain/2d-terrain-with-path.png)

# ![Mesh Terrain](/assets/images/posts/visualizing-terrain/mesh-terrain.png)


---

## How to Use
1. Open the notebook (`terrain_gen.ipynb`) in Jupyter or VS Code.
2. Run all cells to generate terrain, compute the path, and view visualizations.
3. (Optional) Extend with interactive controls for terrain editing or obstacle placement.

---

## Educational Value & Learning Outcomes
- Deepens understanding of algorithmic thinking, optimization, and spatial data analysis
- Demonstrates practical use of Python for scientific computing and visualization
- Provides a foundation for further exploration in pathfinding, terrain analysis, or interactive applications
- Clean, modular, and well-documented for both self-study and professional presentation

---

## Possible Next Steps
- Add interactive widgets for real-time terrain editing and obstacle placement.
- Enable exporting of terrain and path data.
- Further polish documentation and add user instructions.

---

**Project by MylesTym**

[LinkedIn](https://www.linkedin.com/in/myles-tym/) | [GitHub](https://github.com/MylesTym)
