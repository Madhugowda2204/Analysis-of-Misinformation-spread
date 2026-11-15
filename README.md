# Analysis of Misinformation Spread

An interactive network visualization project that explores how information can travel through a directed network. Built with Python, NetworkX, Dash and Plotly, the application displays network connections and lets users explore selected target nodes with an animated path visualization.

## Project Overview

The project reads an edge list from a CSV file and represents it as a directed graph. Each row connects a `source` node to a `target` node.

The interactive dashboard provides:
- **2D and 3D layouts** to view the network in different ways.
- **Directed network visualization** to explore connections between nodes.
- **Node selection** through a multi-select dropdown.
- **Predecessor subgraphs** to view selected target nodes and their immediate predecessors.
- **Shortest-path exploration** between a selected predecessor and its target.
- **Animated information flow** along the calculated path.

## Technologies Used

- Python
- NetworkX
- Pandas
- NumPy
- Dash
- Plotly

## Repository Files

```text
Analysis-of-Misinformation-spread/
├── main.py
├── updated.csv
├── requirements.txt
└── README.md
```

## Dataset

The application loads the dataset from `updated.csv` in the project directory.

The CSV must contain these columns:
- `source` — the starting node of a connection.
- `target` — the node connected to the source.

The current graph-building code uses the `source` and `target` columns to create the directed network.

## Setup and Installation

1. Clone or download this repository.
2. Open a terminal in the project directory.
3. (Recommended) Create and activate a Python virtual environment.
4. Install the required libraries:

```bash
pip install -r requirements.txt
```

## Run the Application

Make sure `updated.csv` and `main.py` are in the same directory, then run:

```bash
python main.py
```

Open the local address shown in the terminal to use the Dash dashboard.

## How to Use

1. Start the application.
2. Choose either **2D Layout** or **3D Layout**.
3. Select one or more target nodes from the dropdown.
4. Explore the main network and the corresponding predecessor subgraph.
5. Use **Play Animation** in the subgraph to view the animated path.

## Project Scope

This implementation visualizes relationships in the dataset as a directed network. Although the dataset may contain other information, the current Python code builds the graph from the `source` and `target` columns; it does not currently perform text-based misinformation classification or use the `label` and `text` fields in its graph calculations.
