# Metro Map Visualizer

This repository provides an interactive visualization of metro networks, including metro lines, stations, and some information about the underground topography.

---

## Overview

The **Metro Map Visualizer** is a web-based application that dynamically visualizes metro lines, station depths, altitudes, transfer stations, and additional information about each metro stop.

It is designed to visualize the information contained in the `metro-data.json` file.

---

## Usage

### Download the Repository

Clone the repository and navigate to the directory:

```bash
git clone https://github.com/daviligade/metro_network_viewer
cd metro_network_viewer
```

### Running the Server

Ensure you have Python installed. Start the local server with:

```bash
python3 server.py
```

Open your web browser and navigate to:

```
http://localhost:8000/metro_network_viewer.html
```

---

## 🎬 Demo

Here's a quick demo of the Metro Network Visualizer in action with fictional data:

<p align="center">
  <img src="https://i.imgur.com/CVs89z4.gif" width="800px" alt="Metro Visualizer Demo">
</p>



---

## Data Structure

The visualization relies on a structured JSON file (`metro-data.json`) that includes detailed metro information. The JSON structure is as follows:

### Metro Information

- **`metroName`**: Name of the metro network.
- **`metroInfo`**: Descriptive and historical context (e.g. opening year, length, ridership).

### Lines

Each metro line includes:
- **`color`**: Hex color used for visualization.
- **`name`**: Line designation.
- **`info`**: Historical and operational specifics.
- **`stops`**: List of stations with:
  - Name, map coordinates (`mapX`, `mapY`).
  - Depth and altitude data.
  - Distance from previous station.
  - Facilities, accessibility, daily passenger count, etc.

### Transfer Stations

- Stations shared between multiple lines, including:
  - Station name, intersecting lines.
  - Descriptive information (e.g., facilities, and coordinates).

---

## Adapting to Different Metro Networks

To adapt the visualizer for different metro networks:

1. Prepare your JSON file following the existing structure (`metro-data.json`).
2. Include relevant details such as coordinates, depth, altitude, and station information.
3. Update or replace the existing `metro-data.json` with your new one.

---

## Requirements

- **Browser Compatibility**: Modern browsers supporting HTML5, SVG, CSS3, JavaScript.
- **Local Server**: Python (`server.py` included).

---

## Features and to-do list

- **Interactive Metro Map [level 1]**:
  - [X] Schematic overview with clickable lines.
  - [X] Zoomable interface.
  - [X] Highlighting lines and stations upon hover, including transfer stations.
  - [X] Special highlighting for transfer stations.

- **Detailed Line View [level 2]**:
  - [X] Horizontal detailed representation showing distances and elevations.
  - [X] Visual depiction of altitude, sea level, and underground station depth.
  - [X] Detailed information for each line visualized as additional info.
  - [X] Possibility to filter lines' stops with a "filters" button.

- **Detailed Information about each Stop/Station [level 3]**:
  - [X] Detailed information for each stop/station.

- **Adaptability**:
  - [X] Easily adaptable to visualize other metro systems by changing data files (changing the `metro-data.json` file).

---

Enjoy visualizing your metro networks interactively!

