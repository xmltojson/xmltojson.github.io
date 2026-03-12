# 🏰 The Maze Generator

An interactive maze generator and solver built with vanilla JavaScript, HTML5 Canvas, and CSS. Generate mazes of various sizes, solve them with AI algorithms, play manually, or watch an automated demo — all in your browser.

**[▶ Live Demo](https://mazegenerator.github.io)**

![Maze Generator Screenshot](https://img.shields.io/badge/status-live-brightgreen) ![License](https://img.shields.io/badge/license-MIT-blue)

---

## ✨ Features

### 🔄 Maze Generation
- Recursive backtracker algorithm for perfect maze generation
- Configurable sizes from 10×10 to 50×50
- Instant generation with visual rendering

### 🤖 AI Solvers
- **DFS** — Depth-First Search with randomized neighbor exploration
- **BFS** — Breadth-First Search for shortest path guarantee
- **A\*** — A-Star with Manhattan distance heuristic for optimal pathfinding
- Adjustable animation speed (1–100)
- Real-time visualization of visited cells, current position, and solution path

### 🎮 Manual Play
- Navigate the maze using keyboard (Arrow keys / WASD), touch swipe, or click/tap on adjacent cells
- Automatic backtrack detection — retracing steps removes them from your path
- Live timer and step counter
- Victory modal with stats (time, steps, path length, maze size)
- Confetti celebration on completion 🎉

### 🎬 Demo Mode
- Automated showcase cycling through all sizes (10×10 → 50×50)
- Rotates between DFS, BFS, and A* solvers
- 2-second pause between each maze for viewing the solution
- Loops continuously until stopped

### 🔍 Zoom & Pan
- **Pinch-to-zoom** on touch devices
- **Mouse wheel** zoom on desktop
- **Drag/pan** to navigate large mazes
- Auto-fit and center on generation and window resize

### 📱 Responsive Design
- Fully adaptive layout for phones, tablets, and desktops
- Fluid typography with `clamp()` scaling
- Dynamic viewport height (`100dvh`) for mobile browser compatibility
- Touch-optimized controls and interactions

### 💾 Persistent State
- Maze state saved to `localStorage` automatically
- Restores maze, player position, path, and timer on page reload

---

## 🚀 Getting Started

### Play Online

Visit **[mazegenerator.github.io](https://mazegenerator.github.io)** — no installation required.

### Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/mazegenerator/mazegenerator.github.io.git
   ```

2. Open `index.html` in your browser:

   ```bash
   cd mazegenerator.github.io
   open index.html
   ```

No build tools, dependencies, or server required — it's a single HTML file.

---

## 🎯 How to Use

| Action | Description |
|---|---|
| **🔄 New** | Generate a new random maze |
| **🤖 AI** | Run the selected AI solver with animation |
| **🎮 Play** | Enter manual mode — navigate to the star ⭐ |
| **🎬 Demo** | Start automated demo (10×10 → 50×50) |
| **🗑️ Clear** | Reset solve/play state, keep the maze |

### Controls in Manual Mode

| Input | Action |
|---|---|
| `↑` `↓` `←` `→` | Move player |
| `W` `A` `S` `D` | Move player |
| Swipe | Move player (touch) |
| Tap adjacent cell | Move player (touch/mouse) |
| Pinch | Zoom in/out |
| Drag (2 fingers or mouse) | Pan the view |

---

## 🛠️ Technology

- **HTML5 Canvas** — maze rendering and animations
- **Vanilla JavaScript** — no frameworks or dependencies
- **CSS3** — gradients, animations, responsive layout
- **localStorage** — state persistence
- **Single file** — entire application in one `index.html`

---

## 📐 Algorithms

### Maze Generation — Recursive Backtracker
A randomized depth-first search that carves passages through a grid, guaranteeing a perfect maze (exactly one path between any two cells).

### Solving — DFS
Explores as deep as possible along each branch before backtracking. Fast but does not guarantee the shortest path.

### Solving — BFS
Explores all neighbors at the current depth before moving deeper. Guarantees the shortest path in an unweighted maze.

### Solving — A*
Uses a priority queue with `f(n) = g(n) + h(n)` where `h` is the Manhattan distance to the goal. Finds the optimal path while typically exploring fewer cells than BFS.

---

## 📁 Project Structure

```
mazegenerator.github.io/
├── index.html    # Entire application (HTML + CSS + JS)
├── README.md     # This file
└── LICENSE       # MIT License
```

---

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'Add my feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<p align="center">
  Made with ❤️ using vanilla JavaScript
  <br>
  <a href="https://mazegenerator.github.io">mazegenerator.github.io</a>
</p>
