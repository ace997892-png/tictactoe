# Tic Tac Toe

A Python tic-tac-toe game built with tkinter, featuring local 2-player mode and a bot opponent.

## Features

- **Intro screen** — welcome screen with a Play button before entering the game
- **2-player mode** — enter custom names for Player 1 and Player 2
- **Bot opponent** — toggle a checkbox to play against a bot instead of a second human. The bot prioritizes winning moves, then blocking the opponent, then strategic positioning (center, then corners)
- **Score tracking** — wins are tracked across rounds and displayed on screen
- **Hover effects** — empty tiles highlight when you mouse over them
- **Winning line animation** — the winning row/column/diagonal flashes before highlighting
- **Restart vs. New Match** — "Restart" clears the board but keeps score and names; "New Match" resets everything, including player names and score

## How to run

Requires Python 3 with tkinter (included by default in most Python installations).## How it works

- The board is stored as a 3x3 list of tkinter Button widgets
- `check_winner()` checks all 8 possible winning lines (3 rows, 3 columns, 2 diagonals) using a single loop instead of separate code for each direction
- The bot's move logic (`bot_move()` and `find_winning_move()`) checks: can I win this turn? → can I block the opponent from winning? → take the center → take a corner → take any open tile

## Possible future improvements

- Networked multiplayer across separate devices
- Difficulty levels for the bot (e.g., a fully unbeatable version using the minimax algorithm)
- Canvas-drawn X/O graphics instead of text characters