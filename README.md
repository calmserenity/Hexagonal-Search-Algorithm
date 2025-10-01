# Hexagonal Maze Exercise - Assignment 2

## Overview
This project implements a solution for navigating a hexagonal grid maze to collect all treasures while dealing with various traps and rewards that affect movement costs and abilities.

## Problem Description
- **Goal**: Collect all treasures in a hexagonal grid maze
- **Navigation**: 6-directional movement on hex grid
- **Challenges**: Dynamic costs affected by traps and rewards

### Game Elements
- **Treasures**: Items to collect (goal is to collect all)
- **Traps**: 
  - Trap 1: Doubles gravity multiplier
  - Trap 2: Doubles speed multiplier  
  - Trap 3: Forces movement 2 cells in last direction
  - Trap 4: Removes all uncollected treasures from map
- **Rewards**:
  - Reward 1: Halves gravity multiplier
  - Reward 2: Halves speed multiplier

### State Representation
The game state includes:
- Current position
- Set of collected treasures
- Gravity multiplier (affects movement cost)
- Speed multiplier (steps needed for next move)
- Last movement direction
- Available treasures, traps, and rewards on the map

## Algorithm
The solution uses **A* search** algorithm for optimal pathfinding with:
- Dynamic cost calculation: `gravity_multiplier * speed_multiplier`
- Heuristic function for efficient search

## Requirements
- Python >= 3.12
- matplotlib >= 3.10.3
- numpy >= 2.2.6
- streamlit >= 1.45.1

## Installation
```bash
# Install dependencies using uv
uv sync

# Or using pip
pip install -r requirements.txt
```

## Usage
```bash
python main.py
```

## Development
```bash
# Install development dependencies
uv sync --group dev

# Run linter
ruff check .
```

## Project Structure
```
├── main.py          # Main application entry point
├── docs/            # Documentation and assignment instructions
├── pyproject.toml   # Project configuration
└── README.md        # This file
```

## Project Outcome
<img width="939" height="592" alt="image" src="https://github.com/user-attachments/assets/e254bb62-4ecd-49a1-8165-4fe7698f867c" />
