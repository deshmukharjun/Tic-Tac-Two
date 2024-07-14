
# TicTacTwo Android Game

TicTacTwo is an enhanced version of the classic Tic-Tac-Toe game for Android, developed in collaboration with Vishesh Bhandare. This version includes several new features and improvements to provide a more engaging and strategic gameplay experience.

## Features

- Two-player game
- Alternating turns between players (X and O)
- Move limitation mechanic: Only the last three moves of each player are visible on the board
- Win detection for rows, columns, and diagonals
- Tie detection
- Game restart functionality
- Dark mode for a better user experience
- Enhanced UI for improved visual appeal

## Installation

1. Clone the repository to your local machine:
    ```sh
    git clone https://github.com/deshmukharjun/tictactwo.git
    ```
2. Open the project in Android Studio.
3. Build and run the project on an emulator or physical device.

## Usage

1. Launch the app on your Android device.
2. Tap on an empty cell to make a move.
3. Players take turns tapping on empty cells.
4. Only the last three moves of each player are visible on the board; the fourth move causes the oldest move to vanish.
5. The game will display a message when a player wins or if the game ends in a tie.
6. Press the "Restart" button to reset the game.

## Code Overview

### MainActivity.java

- **Variables**:
  - `activePlayer`: Tracks the current player (0 for X, 1 for O).
  - `gameState`: Array to store the state of the board (0 for X, 1 for O, 2 for empty).
  - `winPositions`: Array of winning positions.
  - `gameActive`: Boolean to track if the game is active.
  - `xMoves`, `oMoves`: Queues to track the last three moves of each player.

- **Methods**:
  - `playerTap(View view)`: Handles player taps on the board, updates the game state, manages the move limitation mechanic, and checks for a win or tie.
  - `checkGameStatus()`: Checks the current state of the game to determine if there is a win or tie.
  - `restartGame(View view)`: Resets the game to its initial state.
  - `ChangeMode(View view)`: Toggles between light and dark modes.
  - `updateTheme()`: Updates the UI theme based on the current mode.
  - `ShowInfo(View view)`: Displays the information overlay.
  - `HideInfo(View view)`: Hides the information overlay.

- **Lifecycle**:
  - `onCreate(Bundle savedInstanceState)`: Initializes the activity, sets up UI components, loads saved theme preferences, and hides the restart button.

## Acknowledgments

- This project was developed as a learning exercise for Android development.
- Icons and images are sourced from [source].
- Special thanks to Vishesh Bhandare for his collaboration and contributions.
