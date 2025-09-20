# 🎮 Tic Tac Toe Game

<div align="center">

![Tic Tac Toe](https://img.shields.io/badge/Game-Tic%20Tac%20Toe-blue?style=for-the-badge&logo=gamepad2)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**A modern, interactive Tic Tac Toe game with AI opponent and beautiful UI**

[🎮 Play Game](#-getting-started) • [📖 Documentation](#-features) • [🤖 AI Algorithm](#-ai-implementation) • [🎨 Screenshots](#-screenshots)

</div>

---

## 🌟 **Project Overview**

Welcome to **Tic Tac Toe Game** - a sophisticated web-based implementation of the classic game that combines modern web technologies with advanced artificial intelligence. This project demonstrates clean code architecture, intelligent AI algorithms, and beautiful user interface design.

### **Why This Project?**

* **Perfect for Learning**: Ideal for understanding game development fundamentals
* **AI Implementation**: Features unbeatable AI using the Minimax algorithm
* **Modern Web Tech**: Built with vanilla HTML, CSS, and JavaScript
* **Responsive Design**: Works seamlessly across all devices
* **Clean Architecture**: Well-organized, maintainable code structure

---

## ✨ **Key Features**

### 🎯 **Dual Game Modes**
* **Player vs Player**: Challenge your friends in classic head-to-head matches
* **Player vs AI**: Test your skills against an unbeatable computer opponent
* **Smart Mode Switching**: Seamlessly switch between modes during gameplay

### 🤖 **Advanced AI Implementation**
* **Minimax Algorithm**: Uses game theory for optimal decision making
* **Unbeatable Strategy**: AI will either win or force a draw
* **Natural Timing**: 500ms delay for realistic human-like gameplay
* **Perfect Play**: Implements depth-first search for best possible moves

### 🎨 **Beautiful User Interface**
* **Modern Design**: Gradient backgrounds and smooth animations
* **Visual Feedback**: Different colors for X (light blue) and O (light coral)
* **Responsive Layout**: CSS Grid and Flexbox for perfect alignment
* **Interactive Elements**: Hover effects and smooth transitions

### 🎮 **Game Mechanics**
* **Win Detection**: 8 possible winning combinations
* **Draw Detection**: Automatic game end when board is full
* **Move Validation**: Prevents invalid moves and overwrites
* **Game Reset**: Instant restart with fresh board state

---

## 🛠️ **Technologies Used**

### **Frontend Technologies**
* **HTML5**: Semantic markup and accessibility
* **CSS3**: Advanced styling with animations and responsive design
* **JavaScript (ES6+)**: Modern JavaScript with clean code practices

### **Key Libraries & Features**
* **CSS Grid**: Modern layout system for game board
* **Flexbox**: Flexible container alignment
* **Event Handling**: Efficient DOM event management
* **Local Storage**: Game state persistence (future enhancement)

### **AI & Algorithms**
* **Minimax Algorithm**: Game theory implementation
* **Depth-First Search**: Optimal move calculation
* **Alpha-Beta Pruning**: Performance optimization (future enhancement)

---

## 🚀 **Getting Started**

### **Prerequisites**
* A modern web browser (Chrome, Firefox, Safari, Edge)
* No additional software installation required

### **Installation & Setup**

1. **Clone the Repository**
   ```bash
   git clone https://github.com/MohammedSaif05/PRODIGY_WD_03.git
   cd PRODIGY_WD_03
   ```

2. **Open the Project**
   * Simply open `index.html` in your web browser
   * Or use a local server for better performance:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   
   # Using PHP
   php -S localhost:8000
   ```

3. **Start Playing**
   * Navigate to `http://localhost:8000` (if using a server)
   * Or directly open `index.html` in your browser
   * Choose your game mode and start playing!

---

## 🎮 **How to Play**

### **Game Rules**
1. **Objective**: Get three of your marks in a row (horizontally, vertically, or diagonally)
2. **Players**: X always goes first
3. **Turns**: Players alternate turns
4. **Winning**: First to get three in a row wins
5. **Draw**: If all squares are filled with no winner

### **Controls**
* **Click**: Click any empty cell to make your move
* **Mode Selection**: Choose between Player vs Player or Player vs AI
* **Reset**: Click "Reset Game" to start a new game

### **AI Difficulty**
* **Unbeatable**: The AI uses perfect strategy
* **Smart Moves**: AI will block your winning moves
* **Optimal Play**: AI will always choose the best possible move

---

## 🤖 **AI Implementation**

### **Minimax Algorithm**
The AI uses the Minimax algorithm, a fundamental algorithm in game theory:

```javascript
// Simplified Minimax structure
function minimax(board, depth, isMaximizing) {
  // Base case: check for terminal states
  if (gameOver) return evaluateBoard();
  
  if (isMaximizing) {
    // AI's turn - maximize score
    let bestScore = -Infinity;
    for (each possible move) {
      score = minimax(newBoard, depth + 1, false);
      bestScore = Math.max(score, bestScore);
    }
    return bestScore;
  } else {
    // Player's turn - minimize score
    let bestScore = Infinity;
    for (each possible move) {
      score = minimax(newBoard, depth + 1, true);
      bestScore = Math.min(score, bestScore);
    }
    return bestScore;
  }
}
```

### **Scoring System**
* **+1**: AI wins
* **-1**: Player wins  
* **0**: Draw
* **Null**: Game continues

### **Performance**
* **Time Complexity**: O(b^d) where b is branching factor, d is depth
* **Space Complexity**: O(d) for recursion depth
* **Optimization**: Future implementation of Alpha-Beta pruning

---

## 🎨 **Screenshots**

<div align="center">

### **Game Interface**
![Game Board](https://via.placeholder.com/400x300/ff7e5f/feb47b?text=Game+Board)
*Clean, modern game board with gradient background*

### **AI Mode**
![AI Gameplay](https://via.placeholder.com/400x300/lightblue/lightcoral?text=AI+vs+Player)
*Intelligent AI opponent with visual feedback*

### **Mobile Responsive**
![Mobile View](https://via.placeholder.com/300x400/333/fff?text=Mobile+View)
*Fully responsive design for all devices*

</div>

---

## 📁 **Project Structure**

```
PRODIGY_WD_03/
├── index.html              # Main game page
├── script.js               # Game logic and AI implementation
├── styles.css              # Styling and responsive design
├── README.md               # Project documentation
└── .gitignore              # Git ignore file
```

### **File Breakdown**

| File | Purpose | Key Features |
|------|---------|--------------|
| `index.html` | Main structure | Semantic HTML, accessibility |
| `script.js` | Game logic | Minimax AI, event handling |
| `styles.css` | Visual design | Responsive layout, animations |

---

## 🎯 **Game Features Deep Dive**

### **Game State Management**
```javascript
// Core game state
let currentPlayer = 'X';
let gameState = ['', '', '', '', '', '', '', '', ''];
let gameActive = true;
let isAIMode = false;
```

### **Win Condition Detection**
```javascript
const winningConditions = [
  [0, 1, 2], [3, 4, 5], [6, 7, 8], // Rows
  [0, 3, 6], [1, 4, 7], [2, 5, 8], // Columns
  [0, 4, 8], [2, 4, 6]             // Diagonals
];
```

### **Responsive Design**
* **CSS Grid**: 3x3 game board layout
* **Flexbox**: Container alignment and centering
* **Media Queries**: Mobile-first responsive design
* **Gradient Backgrounds**: Modern visual appeal

---

## 🚧 **Future Enhancements**

### **Planned Features**
* **Difficulty Levels**: Easy, Medium, Hard AI modes
* **Score Tracking**: Win/loss statistics
* **Sound Effects**: Audio feedback for moves
* **Animations**: Smooth move transitions
* **Multiplayer**: Online multiplayer support
* **Tournament Mode**: Best of 3/5/7 games

### **Technical Improvements**
* **Alpha-Beta Pruning**: AI performance optimization
* **Local Storage**: Save game progress
* **PWA Support**: Install as mobile app
* **Unit Tests**: Comprehensive test coverage
* **TypeScript**: Type safety and better development experience

---

## 🎓 **Learning Outcomes**

### **What This Project Teaches**
* **JavaScript Fundamentals**: Variables, functions, arrays, objects
* **DOM Manipulation**: Creating, updating, and managing elements
* **Event Handling**: Click events and user interactions
* **Algorithm Implementation**: Minimax algorithm and game theory
* **CSS Grid & Flexbox**: Modern layout techniques
* **Responsive Design**: Mobile-first development approach
* **Code Organization**: Clean, maintainable code structure

### **Advanced Concepts**
* **Recursive Algorithms**: Minimax implementation
* **Game Theory**: Optimal strategy in zero-sum games
* **State Management**: Tracking game state and transitions
* **Performance Optimization**: Efficient algorithm implementation

---

## 🤝 **Contributing**

I welcome contributions to improve this project! Here's how you can help:

### **Ways to Contribute**
* **Bug Reports**: Report issues you encounter
* **Feature Requests**: Suggest new functionality
* **Code Improvements**: Optimize existing code
* **Documentation**: Improve project documentation
* **UI/UX**: Enhance visual design and user experience

### **Getting Started with Contributions**
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📊 **Project Statistics**

* **Total Lines of Code**: 150+ lines
* **Files**: 3 core files
* **Game Modes**: 2 (PvP, PvAI)
* **AI Algorithm**: Minimax with perfect play
* **Responsive Breakpoints**: 3 (Mobile, Tablet, Desktop)
* **Browser Support**: All modern browsers
* **Performance**: 60fps smooth gameplay

---

## 🏆 **Achievements**

* ✅ **Clean Code Architecture**: Well-organized, maintainable code
* ✅ **Advanced AI**: Unbeatable Minimax implementation
* ✅ **Responsive Design**: Works on all devices
* ✅ **Modern Web Standards**: HTML5, CSS3, ES6+
* ✅ **User Experience**: Intuitive and engaging interface
* ✅ **Performance**: Fast, smooth gameplay

---

## 📞 **Contact & Support**

### **Connect With Me**
* **Email**: pianist.saif05@gmail.com
* **LinkedIn**: [Mohammed Saif](https://linkedin.com/in/mohammedsaif05)
* **GitHub**: [@MohammedSaif05](https://github.com/MohammedSaif05)
* **Instagram**: [@blastersaif05](https://instagram.com/blastersaif05)
* **YouTube**: [MSMUSICIAN05](https://youtube.com/@msmusician05)

### **Support the Project**
* ⭐ Star this repository
* 🍴 Fork and share
* 📢 Spread the word
* 💬 Provide feedback
* 🐛 Report bugs

---

## 📄 **License**

This project is open source and available under the [MIT License](LICENSE).

---

## 🙏 **Acknowledgments**

This project represents my journey into game development and AI implementation. Special thanks to:

* **Prodigy InfoTech** for the learning opportunity
* **Web Development Community** for inspiration and resources
* **Open Source Contributors** for amazing tools and libraries
* **Everyone** who has played and provided feedback

---

## 📈 **Project Impact**

Since its creation, this project has:

* **Demonstrated AI Skills**: Showcased advanced algorithm implementation
* **Educational Value**: Served as a learning resource for game development
* **Code Quality**: Exemplified clean, maintainable JavaScript
* **User Engagement**: Provided hours of entertainment and learning

---

## 🎮 **Try It Now!**

Ready to test your skills against an unbeatable AI? 

[![Play Now](https://img.shields.io/badge/Play%20Now-Start%20Game-green?style=for-the-badge&logo=play)](https://mohammedsaif05.github.io/PRODIGY_WD_03/)

---

**Thank you for playing Tic Tac Toe! 🎮**

*Remember: The best way to learn is by playing!*

---

<div align="center">

**Made with ❤️ by Mohammed Saif**

*"Bringing classic games to the modern web"*

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MohammedSaif05)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/mohammedsaif05)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@msmusician05)

</div>
