# Krakow Transport Network Analysis

**Combining GTFS and OSM Data to Identify Critical Infrastructure**

---

## Overview

This project analyzes Krakow's transport network by combining:
- **GTFS data**: Public transport schedules and routes
- **OSM data**: Street network infrastructure

The goal is to identify critical nodes and segments using graph centrality metrics and to visualize the integrated network.

---

## Features

- **GTFS Data Loading & Preprocessing**: Reads and prepares public transport data.
- **OSM Data Integration**: Downloads and processes Krakow’s street network.
- **Segment Utilization Analysis**: Calculates and visualizes the busiest and least-used segments.
- **Network Graph Construction**: Builds a stop-to-stop directed graph and computes centrality measures.
- **Multimodal Network Integration**: Merges public transport and road networks for holistic analysis.
- **Centrality Analysis**: Computes eigenvector, PageRank, betweenness, and degree centralities for nodes and edges.
- **Critical Node Identification**: Highlights the most important nodes for network resilience.
- **Interactive Visualizations**: Generates interactive maps and charts (HTML output) for all key analyses.

---

## Project Structure

```
.
├── krakow_transport_analysis.ipynb   # Main analysis notebook
├── gtfs/                            # GTFS data (unzipped)
├── gtfs.zip                         # GTFS data (zipped, optional)
├── results/
│   ├── gtfs_graph/                  # GTFS-based analysis outputs
│   ├── osm_graph/                   # OSM-based analysis outputs
│   └── merged_gtfs_osm/             # Multimodal network outputs
├── img/                             # Images and figures
└── README.md                        # This file
```

---

## Getting Started

### 1. Requirements

- Python 3.8+
- Recommended packages:
    - pandas, numpy, networkx, osmnx, geopandas, matplotlib, plotly, folium, shapely, scipy, joblib

Install all dependencies with:

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install pandas numpy networkx osmnx geopandas matplotlib plotly folium shapely scipy joblib
```

### 2. Data

- Place your **GTFS zip file** as `gtfs.zip` in the project root.
- The notebook will extract it automatically to `gtfs/` if not already present.

---

## How to Run

1. Open `krakow_transport_analysis.ipynb` in Jupyter Notebook or VS Code.
2. Run all cells step by step.
3. Outputs (interactive maps, charts, CSVs) will be saved in the `results/` subfolders.

---

## Key Analysis Steps

1. **Load and Prepare GTFS Data**  
   Reads GTFS files, preprocesses shapes and trips.

2. **Analyze Transit Operations**  
   Counts trips per route/direction, visualizes busiest lines.

3. **Preprocess Route Shapes**  
   Converts shape points into route segments.

4. **Calculate Segment Utilization**  
   Aggregates trip counts per road segment, identifies top and bottom segments.

5. **Build Stop Network Graph**  
   Constructs a directed graph of stops, computes centrality measures.

6. **Integrate OSM Street Data**  
   Downloads Krakow’s road network, converts to graph.

7. **Create Multimodal Network**  
   Merges GTFS and OSM graphs, assigns flow capacities.

8. **Assigning Flow Capacities**  
   Assigns flow capacities to network edges based on road type and bus frequency.

9. **Multimodal Centrality Analysis**  
   Calculates eigenvector, PageRank, betweenness, and degree centralities for nodes and edges.

10. **Critical Node Analysis**  
    Identifies and visualizes the most important nodes for network resilience.
---

## Outputs

- **Interactive HTML maps**: In `results/`, e.g. `2_trips_per_route_direction.html`, `4_5_segment_trip_distribution_interactive.html`, etc.
- **CSV files**: Centrality measures and statistics.
- **Plots and charts**: For all major steps.

---

## Notes

- Some output HTML files may be large (>50MB) and are best viewed locally.
- For large files, consider using [Git LFS](https://git-lfs.github.com/).
- All code is modular and can be adapted for other cities or datasets.

---

## License

MIT License

---

## Acknowledgements

- [OSMnx](https://github.com/gboeing/osmnx)
- [GTFS](https://developers.google.com/transit/gtfs)
- [Folium](https://python-visualization.github.io/folium/)
- [Plotly](https://plotly.com/python/)

---

*Created as part of a master's project on urban transport network analysis.*