# Snektris · Snake × Tetris

**▶ Play online: https://mastercormac.github.io/snektris/**

Snektris fuses the two most iconic single-player mobile games of all time — **Tetris (1984)** and **Snake (1976 / Nokia era)** — into a single 10×20 board: tetrominoes fall, stack, and clear lines as usual, while a snake slithers through the gaps hunting apples, and can even chew through misplaced blocks to save a bad stack. It shows that two classics nearly half a century old still spark new gameplay chemistry when combined. Single-file, zero-dependency, playable on mobile.

## How to Play

- **Tetris**: 7 standard tetrominoes fall automatically; move, rotate, and drop them with the arrow keys or on-screen buttons. Clear lines to score; more lines = higher level = faster fall speed.
- **Snake**: the snake moves at a fixed pace; steer it with WASD or by swiping on the board. Eating an 🍎 scores +50 and grows the snake by 2 segments.
- **The fusion**:
  - Some falling pieces hide an apple (marked with a red frame) — once the piece locks, the apple stays on the board and the snake must climb up to eat it;
  - The snake can **chew through** settled blocks (+10, snake length −1) — an emergency escape hatch for a messy stack, but chew too much and the snake gets too short to survive;
  - Hitting a wall or itself costs −100 points and respawns the snake at the bottom; the game ends only when the stack reaches the top.
  - Watch out — a locking tetromino can crush the snake.

## Controls

| Platform | Tetromino | Snake |
|---|---|---|
| Keyboard | ← → move, ↑ rotate, ↓ soft drop, Space hard drop | W A S D |
| Mobile | On-screen buttons | Swipe on the board |

The snake starts dormant (rendered semi-transparent) — press WASD or swipe to wake it.

## Run Locally

No build step needed — just open `index.html` in a browser, or serve it statically:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy to GitHub Pages

```bash
git init && git add . && git commit -m "Snektris: snake x tetris mashup"
git branch -M main
git remote add origin https://github.com/<your-username>/snektris.git
git push -u origin main
```

Then go to **Settings → Pages → Source**, pick the `main` branch root, and your game will be live at `https://<your-username>.github.io/snektris/` within minutes.

## Tech

Single-file HTML + Canvas + vanilla JS, zero dependencies, ~400 lines. MIT License.
