# Snake

A woodland-themed Snake game with 20 progressive levels, an AI explorer, procedurally illustrated graphics, and responsive desktop and mobile controls.

## Demo

Play the game: [snakegamej.github.io](https://snakegamej.github.io)

## Features

- **20 Progressive Levels** — Gather more apples and navigate increasingly rocky terrain.
- **Woodland Graphics** — Procedurally drawn grass, leaves, rocks, apples, and a textured, smoothly animated snake.
- **AI Explorer** — Watch the snake navigate using pathfinding and escape-route planning.
- **Responsive Design** — Viewport-fitted desktop layout with compact panels and a square game board. Mobile and very short windows use natural scrolling.
- **Touch Controls** — Swipe gestures and on-screen direction buttons.
- **Keyboard Controls** — Arrow keys or WASD for movement.
- **Auto-Save** — Active games are saved locally and restored in a paused state.
- **Trail Records** — Keep up to 20 completed-level records with paginated navigation.
- **Pause/Resume** — Pause manually or automatically when leaving the browser tab.
- **Optional Audio** — Synthesized tones for collecting apples, completing levels, and losing.
- **Guide Grid** — Toggle a grid to help plan your route.
- **Reduced-Motion Support** — Respects your device’s reduced-motion preference.
- **No Build Dependencies** — Game graphics and audio are generated directly in the browser.

## How to Play

1. Choose a **Starting level**, or begin at Level 1 for the full adventure.
2. Click **Start** or **Enter the clearing**. You can also press **Spacebar** or **Enter** when the game board has focus.
3. Control the snake using:
   - **Desktop:** Arrow keys or WASD.
   - **Mobile:** Swipe gestures or on-screen direction buttons.
4. Collect ripe apples to grow. Each apple is worth one point.
5. Avoid the board edges, rocks, and your own body. Leaves and grass are safe to cross.
6. Reach the level’s apple target before time runs out.
7. Select **Next clearing** or press **Enter** to continue.
8. Complete Level 20 to finish the trail!

After a collision or timeout, select **Try this trail again** to restart the current level.

## Game Mechanics

- The board contains **20 × 20 cells**.
- Each level starts with a **three-segment snake**.
- Apple counts and the timer reset at the beginning of each level.
- Rocks appear from Level 5 onward, reaching a maximum of 15.
- Terrain generation checks that rocks do not create isolated pockets.
- Apples are placed in reachable, unoccupied cells where possible.
- You cannot reverse direction directly into your own body.
- Moving into the tail’s current cell is allowed when the tail moves away on that same turn.

| Level | Target Apples | Time Limit | Rocks |
|-------|---------------|------------|-------|
| 1     | 3             | 108s       | 0     |
| 2     | 6             | 104s       | 0     |
| 3     | 9             | 101s       | 0     |
| 4     | 12            | 97s        | 0     |
| 5     | 15            | 94s        | 2     |
| 6     | 18            | 90s        | 4     |
| 7     | 21            | 108s       | 6     |
| 8     | 24            | 108s       | 8     |
| 9     | 27            | 122s       | 10    |
| 10    | 30            | 135s       | 12    |
| 11    | 33            | 149s       | 14    |
| 12    | 36            | 162s       | 15    |
| 13    | 39            | 176s       | 15    |
| 14    | 42            | 189s       | 15    |
| 15    | 45            | 203s       | 15    |
| 16    | 48            | 216s       | 15    |
| 17    | 51            | 230s       | 15    |
| 18    | 54            | 243s       | 15    |
| 19    | 57            | 257s       | 15    |
| 20    | 60            | 270s       | 15    |

### Time Limit Formula

For level `L`:

```javascript
const target = 3 * L;
const baseTime = Math.max(30, 90 - (L - 1) * 3);

const multiplier = L <= 6
    ? 1.2
    : 1.5 + (L - 7) * 0.5 / 13;

const scaledTime = Math.round(baseTime * multiplier);

const timeLimit = L <= 6
    ? scaledTime
    : Math.max(scaledTime, Math.round(target * 4.5));
```

- **Levels 1–6:** Base time increased by 20%, rounded to whole seconds.
- **Levels 7–20:** The greater of the scaled base time and approximately 4.5 seconds per target apple.
- **AI explorer:** No time limit.

### Movement Speed

Movement timing varies by level.

**Levels 11–20 run at 80% of their original movement speed**, using a 25% longer interval between moves. Levels 1–10 are unchanged.

```javascript
const index = level - 1;

const baseMoveInterval = Math.round(
    Math.max(80, 200 - index * 6) * (1 + 0.2 * index / 19)
);

const speedMultiplier = level >= 11 ? 0.8 : 1;
const moveInterval = baseMoveInterval / speedMultiplier;
```

Intervals are measured in milliseconds. This adjustment affects both manual play and AI exploration; time limits remain unchanged.

## Controls

| Action | Desktop | Mobile |
|--------|---------|--------|
| Move up | ↑ / W | Swipe up / ↑ button |
| Move down | ↓ / S | Swipe down / ↓ button |
| Move left | ← / A | Swipe left / ← button |
| Move right | → / D | Swipe right / → button |
| Start / Retry / Continue | Enter or the action button | Action button |
| Pause / Resume | Spacebar or Pause/Resume button | Pause/Resume button |
| Pause | Escape | Pause button |

Keyboard shortcuts work when the game board or page has focus. Focused buttons, checkboxes, and the level selector retain their normal keyboard behavior.

### Settings

- **AI explorer:** Enable automatic movement.
- **Nature sounds:** Toggle game audio.
- **Guide grid:** Show or hide cell boundaries.

## AI Mode

Enable **AI explorer** to watch the snake play automatically.

The AI uses:

- **Breadth-first search (BFS)** to find routes to apples.
- **Route simulation** to check whether a planned path is safe.
- **Tail-access checks** to look for an escape route after eating.
- **Flood-fill analysis** to evaluate available space.
- **Fallback movement scoring** that favors open areas and access to the tail.

AI exploration has no time limit and automatically advances to the next level after a three-second break. It can still become trapped or collide; successful completion is not guaranteed.

Levels played with AI assistance are excluded from trail records. Enabling AI during an active level marks that level as assisted, even if AI is later disabled.

## Auto-Save and Trail Records

Progress is stored in your browser using `localStorage`.

- Active games are saved periodically and on important state changes.
- Returning to a saved game restores it **paused**, ready to resume.
- Leaving the browser tab pauses active gameplay.
- Settings and the selected level are saved locally.
- Up to **20 unassisted completed-level records** are retained.
- Records are ranked by apple count, then by shortest completion time.
- Pagination keeps records accessible without expanding the desktop sidebar.

Saved data stays in the current browser and is not synchronized between devices. Clearing site data removes saved progress and records. If local storage is unavailable, the game remains playable, but progress may not persist.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/snakegamej/snakegamej.github.io.git
   ```

2. Open the project folder:

   ```bash
   cd snakegamej.github.io
   ```

3. Open `index.html` in a modern browser.

No build process or package installation is required.

## Technologies

- **HTML5 Canvas** — Procedural graphics and game rendering.
- **Vanilla JavaScript** — Gameplay, pathfinding, input handling, and animation.
- **CSS Grid and Flexbox** — Responsive, viewport-aware layout.
- **Web Audio API** — Synthesized game sounds.
- **LocalStorage API** — Saved games, settings, and records.
- **Pointer Events** — Touch gestures and on-screen controls.
- **Page Visibility API** — Automatic pause when leaving the tab.
- **ResizeObserver** — Adaptive board sizing.
- **`requestAnimationFrame`** — Animation and game-loop scheduling.

## License

MIT
