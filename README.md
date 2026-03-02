# 2-Layer Connect 4

A 2-player Connect 4 variant where each cell can hold 2 pieces. Use your 7 special "layer 2" pieces to cover cells and steal your opponent's positions.

## How to Run

**Option 1 — Just open the file:**
Double-click `index.html` in your file explorer.

**Option 2 — Local server:**
```bash
cd connect4-layers
python -m http.server 8000
# Then open http://localhost:8000
```

## How to Play

- **Layer 1:** Click a column to drop a piece (falls to lowest empty slot)
- **Layer 2:** Click "Place Layer 2" to enter special mode, then click any occupied cell to cover it
- Each player gets **7 layer 2 pieces** — use them wisely!
- Only the **top piece** in each cell counts toward winning
- First to get **4 in a row** (any direction) wins
