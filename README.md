# Wikipedia Link Network Analysis

A network analysis project that constructs and analyzes a graph network from Wikipedia article links, exploring centrality measures, community detection, and ego networks.

## Overview

This project builds a network graph from Wikipedia articles and their interconnected links, performing comprehensive network analysis including:
- Network characterization (density, diameter, connectivity)
- Centrality analysis (betweenness, degree, closeness, eigenvector)
- Community detection using the Louvain algorithm
- Ego network analysis for influential nodes
- Network visualization with community coloring

## Requirements

- Python 3.x
- NetworkX
- Matplotlib
- JSON (standard library)

Install dependencies:
```bash
pip install networkx matplotlib
```

## Data Format

The project expects a `wiki.json` file with the following structure:
```json
[
  {
    "article": "Article Name",
    "links": ["Linked Article 1", "Linked Article 2", ...]
  },
  ...
]
```

## Features

### Network Metrics
- **Density**: Measures how interconnected the network is
- **Diameter**: Longest shortest path between any two nodes
- **Connected Components**: Number of disconnected subgraphs

### Centrality Analysis
Identifies the most important nodes using four centrality measures:
- **Betweenness Centrality**: Nodes that act as bridges
- **Degree Centrality**: Nodes with the most connections
- **Closeness Centrality**: Nodes closest to all others
- **Eigenvector Centrality**: Nodes connected to other important nodes

### Community Detection
Uses the Louvain algorithm to identify communities within the network, with visualization showing different communities in distinct colors.

### Ego Networks
Analyzes the local neighborhoods of influential nodes:
- World Health Organization
- Joe Biden
- World War II
- Republic of Ireland
- UEFA
- Leinster Rugby

## Output

The script generates:
- Console output with network statistics and top 10 nodes by each centrality measure
- Multiple visualizations of the full network and community structures
- Individual ego network visualizations
- `ego.gexf` file for import into Gephi for advanced visualization

## Project Structure

```
.
├── GrafosFinal.py      # Main analysis script
├── wiki.json           # Input data file
└── ego.gexf           # Output network file (generated)
```

## Visualization

The project creates several visualizations:
1. Full network graph (120x100 figure)
2. Community-colored network showing detected communities
3. Individual ego networks for each major community hub

## Analysis Components

Based on COMP30850 Network Analysis assignment requirements:
- **Task 1**: Network construction from JSON data
- **Task 2**: Network characterization and centrality analysis
- **Task 3**: Community detection and ego network analysis
- **Task 4**: Network export for Gephi visualization

## License

MIT License - Feel free to use and modify for your own projects.

## Author

Network Analysis Project for COMP30850
