# Snake

A classic Snake game with 20 progressive levels, AI mode, and modern features.

## Demo

Play the game: [https://snakegamej.github.io](https://snakegamej.github.io)

## Features

- **20 Progressive Levels** - Increasing difficulty with more target fruits and obstacles
- **AI Mode** - Watch the AI play with intelligent pathfinding and corner navigation
- **Responsive Design** - Works on desktop and mobile devices
- **Touch Controls** - Swipe gestures and virtual keyboard for mobile play
- **Keyboard Controls** - Arrow keys or WASD for desktop play
- **Auto-Save** - Game state is automatically saved and restored
- **High Scores** - Track your best performances
- **Pause/Resume** - Pause anytime with spacebar or pause button
- **Victory Celebration** - Confetti and fireworks when completing all levels

## How to Play

1. Click **Start Game** or press **Spacebar** to begin
2. Control the snake using:
   - **Desktop**: Arrow keys or WASD
   - **Mobile**: Swipe gestures or virtual buttons
3. Eat fruits to grow and score points
4. Avoid walls, obstacles, and your own tail
5. Reach the target score before time runs out
6. Complete all 20 levels to win!

## Game Mechanics

| Level | Target Fruits | Time Limit | Obstacles |
|-------|---------------|------------|-----------|
| 1     | 3             | 108s       | No        |
| 5     | 15            | 96s        | Yes       |
| 10    | 30            | 78s        | Yes       |
| 15    | 45            | 60s        | Yes       |
| 20    | 60            | 36s        | Yes       |

## Controls

| Action | Desktop | Mobile |
|--------|---------|--------|
| Move Up | ↑ / W | Swipe Up / ▲ |
| Move Down | ↓ / S | Swipe Down / ▼ |
| Move Left | ← / A | Swipe Left / ◄ |
| Move Right | → / D | Swipe Right / ► |
| Pause/Resume | Spacebar | Pause Button |

## AI Mode

Enable AI Mode to watch the snake play automatically. The AI features:

- A* pathfinding algorithm
- Flood fill for survival analysis
- Corner and edge navigation
- Escape route planning
- No time limit in AI mode

## Installation

1. Clone the repository:
```bash
git clone https://github.com/snakegamej/snakegamej.github.io.git
```

2. Open `index.html` in your browser

No build process or dependencies required.

## Technologies

- HTML5 Canvas
- Vanilla JavaScript
- CSS3 Animations
- LocalStorage API

## License

MIT
