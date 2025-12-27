# 🎮 Tic-Tac-Toe with Raylib - Complete C++ Game

## 📋 Overview
A fully graphical **Tic-Tac-Toe game** built with **C++ and Raylib**, featuring mouse controls, smooth visuals, and real-time gameplay. This project transforms the classic console game into an interactive graphical experience with a clean, modern interface.

---

## ✨ Features
- **🎨 Graphical Interface** - Beautiful 600x600 pixel window with clean visuals
- **🖱️ Mouse Controls** - Click to place X/O pieces directly on the board
- **🎯 Real-time Gameplay** - Instant visual feedback for moves
- **🏆 Win Detection** - Automatic detection of wins, losses, and draws
- **🔄 Turn Management** - Alternates between X and O players automatically
- **🎨 Visual Design** - Red X's and Blue O's with clear grid lines
- **⏱️ 60 FPS** - Smooth performance with optimized rendering

---

## 🛠️ Technologies Used
- **C++** - Core game logic and structure
- **Raylib 5.0** - Graphics, window management, and input handling
- **Simple State Management** - Efficient game state tracking

---

## 🚀 How to Compile and Run

### Prerequisites
- **Raylib library** installed
- **C++ compiler** (g++, clang++, or MSVC)
- **Git** (optional, for cloning)

### Installation & Compilation

#### **Option 1: Quick Compile (Linux/macOS)**
```bash
# Install Raylib if not already installed
# Ubuntu/Debian:
sudo apt install libraylib-dev

# Compile the game
g++ -o tictactoe tictactoe.cpp -lraylib -lGL -lm -lpthread -ldl -lrt -lX11

# Run the game
./tictactoe
```

#### **Option 2: Windows (MinGW/MSYS2)**
```bash
# Install Raylib via MSYS2
pacman -S mingw-w64-x86_64-raylib

# Compile
g++ -o tictactoe.exe tictactoe.cpp -lraylib -lopengl32 -lgdi32 -lwinmm

# Run
tictactoe.exe
```

#### **Option 3: macOS**
```bash
# Install Raylib via Homebrew
brew install raylib

# Compile
clang++ -o tictactoe tictactoe.cpp -I/opt/homebrew/include -L/opt/homebrew/lib -lraylib -framework CoreVideo -framework IOKit -framework Cocoa -framework GLUT -framework OpenGL

# Run
./tictactoe
```

---

## 🎮 How to Play
1. **Launch the game** by running the executable
2. **Click on any grid cell** to place your piece
3. **X always goes first**, then O alternates
4. **Win conditions**:
   - Get 3 of your pieces in a row (horizontal, vertical, or diagonal)
   - Block your opponent from getting 3 in a row
5. **Game ends when**:
   - A player gets 3 in a row (X or O wins)
   - All cells are filled with no winner (draw)

---

## 📁 Code Structure
```cpp
// Main Components:
1. board[3][3]        - 3x3 game board storing 'X', 'O', or position numbers
2. drawBoard()        - Draws grid lines and X/O pieces
3. handleMouseClick() - Processes mouse clicks and updates game state
4. Winner Detection   - Checks rows, columns, and diagonals for wins
5. Turn Management    - Alternates between 'X' and 'O' automatically
```

---

## 🎯 Game Logic Details
- **Board Representation**: 3x3 character array initialized with '1'-'9'
- **Mouse Input**: Converts pixel coordinates to grid positions
- **Win Checking**: Checks all 8 possible winning combinations
- **Draw Detection**: When all cells are filled with no winner
- **Turn Switching**: Automatically alternates after each valid move

---

## 🎨 Visual Elements
- **Grid Lines**: Black lines dividing the 3x3 board
- **X Pieces**: Red text centered in each cell
- **O Pieces**: Blue text centered in each cell
- **Win Message**: Displayed at bottom when game ends
- **Background**: Clean white background (RAYWHITE)

---

## 📊 Game States
```
0 = Game in progress
1 = Player X wins
2 = Player O wins
3 = Draw game
```

---

## 🔧 Future Enhancements (Potential)
- Add AI opponent with different difficulty levels
- Implement score tracking across multiple games
- Add sound effects for moves and wins
- Create animated winning line highlight
- Add menu system for restart/quit
- Implement player vs player and player vs AI modes

---

## 🐛 Known Issues
- Game doesn't automatically reset after win/draw
- No input validation for invalid mouse clicks
- Basic visual design (could be enhanced with textures/animations)

---

## 🤝 Contributing
Feel free to fork this repository and submit pull requests with improvements! Some ideas:
- Add difficulty levels for AI
- Implement undo/redo functionality
- Add network multiplayer support
- Create themes/skins for the game

---

## 👤 Author
**Syed Aqdas Munir**  
1st Semester, Artificial Intelligence  
PAF IAST, Mang Haripur, Pakistan

---

## 📄 License
This project is open source and available for educational purposes.

---

## 🎥 Screenshot
```
    X | O | X
    ---------
    O | X | O
    ---------
    7 | O | 9
    
    Player X Wins!
```

---

**Enjoy playing!** 🎮✨
