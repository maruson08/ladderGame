# 🎲 Ladder Simulation - Probability-based Ladder Game in Python
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Matplotlib](https://img.shields.io/badge/matplotlib-%3E%3D3.0-orange)

This project simulates a ladder game with different path rules (`linear`, `round`, and `diagonal`) and visualizes the probabilities of arriving at each endpoint from a selected starting point.

## 📌 Features

- **Three ladder types**:
  - `linear`: a straight ladder where edges are bounded
  - `round`: circular ladder where the first and last columns are connected
  - `diagonal`: any position can jump to any other randomly
- **Simulates multiple trials** from a selected starting position
- **Visualizes**:
  - How frequently each destination is reached
  - A sample of paths taken for each final destination

## 🧪 How to Run

### 1. Install requirements

```bash
pip install matplotlib
```

### 2. Run the simulation

```bash
python Ladder.py
```
## ⚙️ Configuration
The ` config ` dictionary defines the simulation settings: 
```python
config = {
    'depth': 23,             # Vertical depth of the ladder
    'width': 5,              # Number of columns (positions)
    'repeat': 50000,         # Number of simulation repetitions
    'ladder': 'diagonal',    # Ladder type: 'linear', 'round', or 'diagonal'
    'max_display_path': 1    # Max number of sample paths to show per result
}
```
## 📊 Visualization
- **Bar graph** of how many times each destination is reached
- **Red dashed line** for the average arrival count
- **Path traces** for each ending position

## 🧠 Core Functions
| Function                                                    | Description                                                   |
| ----------------------------------------------------------- | ------------------------------------------------------------- |
| `ladder(config, start)`                                     | Simulates one full ladder descent                             |
| `simulate_ladder(config)`                                   | Repeats the simulation `repeat` times and stores all outcomes |
| `_linearLadder`, `_roundLadder`, `_roundLadderWithDiagonal` | Internal logic for ladder step movement                       |
## ✅ Possible Improvements
- Add a GUI (e.g., Tkinter or PyQt) for user interaction
- Fix a random seed for reproducible results
- Save output results and statistics to CSV or image files
- Introduce probabilistic weighting for directional movement
## 📄 License
MIT License

This simulation is developed for educational and experimental purposes.
Feel free to fork, modify, and build upon it!
