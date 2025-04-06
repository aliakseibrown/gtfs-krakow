# GTFS Kraków Network Analysis
## Overview
This repository contains network analysis of Kraków's public transportation system using GTFS (General Transit Feed Specification) data. The project applies graph theory concepts to analyze the connectivity and importance of transit stops throughout the city.

## Data
The analysis uses GTFS data from Kraków's public transportation network, including:

Stop information (locations, names)
Routes and trip data
Stop times and sequences

## Key Features
Network Construction: Builds a directed graph representation of the transit network
Centrality Metrics: Calculates eigenvector centrality and PageRank to identify key transit hubs
Geospatial Visualization: Interactive maps showing stop importance and connections
Weight-based Analysis: Considers connection frequency for edge weights
Methodology
The project follows these analytical steps:

## Data preprocessing and filtering
Construction of a directed graph from stop sequences
Calculation of edge weights based on connection frequency
Application of eigenvector centrality and PageRank algorithms
Visualization of results with geographic context
Visualizations
Interactive Maps: Folium-based visualizations with stops colored by importance metrics
Network Graphs: Representations of the transit network showing connections
Geographic Context: All analysis maintains spatial relationships between stops