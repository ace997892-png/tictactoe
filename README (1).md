# Tic-Tac-Toe (Python + Tkinter)

**Team Members:** Inn Pongwathnak, Heng Piseth, Marin Wathna, Vattanak Bandid, Tea Yioun, Chea Keomoniroath, Kong Kosomak, Ky Rath Tevy, Tang Mingguang, Mony Thiradeth

A classic two-player Tic-Tac-Toe game built with Python's built-in `tkinter` GUI library. Two players take turns clicking cells in a 3x3 grid; the game automatically detects wins (rows, columns, diagonals), highlights the winning line in green, detects a tie (highlighted in yellow), and lets players start a new round at any time.

## Features

- Interactive 3x3 button grid built with Tkinter
- Live turn indicator label at the top of the window
- Automatic win detection across all 8 winning lines (3 rows, 3 columns, 2 diagonals)
- Winning line highlighted in green; a tied board is highlighted in yellow
- One-click "restart" button to reset the board and start a new game

## Prerequisites & Installation

- **Python 3.x** (developed and tested on Python 3.8+)
- **Tkinter** — included with most standard Python installations.
  - Windows / macOS: no action needed, `tkinter` ships with the official Python installer.
  - Linux (Debian/Ubuntu): if `tkinter` is missing, install it with:
    ```bash
    sudo apt-get install python3-tk
    ```

No third-party packages are required — the project only uses Python's standard library (`tkinter`, `random`).

1. Clone the repository:
   ```bash
   git clone <this-repository-url>
   cd <repository-folder>
   ```
2. (Optional) Verify Python is installed:
   ```bash
   python3 --version
   ```

## How to Run

From the repository root, run:

```bash
python3 src/TicTacToe.py
```

(On Windows, `python src/TicTacToe.py` may be used instead, depending on your `PATH` setup.)

A game window will open with the 3x3 board. Click any empty cell to place your mark. The turn label above the board shows whose turn it is; a "restart" button lets you reset the board at any time.

## Project Structure

```
.
├── src/
│   └── TicTacToe.py     # Main game source code
├── docs/                 # (Optional) diagrams / additional documentation
└── README.md             # Project overview and instructions (this file)
```

## How It Works (Technical Overview)

- `buttons` — a 3x3 list holding references to each Tkinter `Button` widget, used to track board state directly from widget text.
- `next_turn(row, column)` — click handler bound to each button; places the current player's mark if the cell is empty and the game hasn't already ended, then switches turns.
- `check_winner()` — checks all rows, columns, and both diagonals for three matching marks; colors the winning cells green, colors the whole board yellow on a tie, and returns `True`, `"Tie"`, or `False` accordingly.
- `empty_spaces()` — counts remaining empty cells to help detect a tie.
- `new_game()` — resets all button text/colors and randomly picks the starting player for a fresh round.

## Future Improvements

- Single-player mode with a computer opponent (e.g., minimax algorithm for unbeatable AI)
- Score tracking across multiple rounds
- Improved visual styling (custom colors, animations, sound effects)
- Network/online multiplayer support
