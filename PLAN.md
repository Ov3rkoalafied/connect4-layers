# 2-Layer Connect 4 — Plan

## What We're Building
A local 2-player Connect 4 variant where each cell can hold 2 pieces (depth layers).
Covering a cell with a layer 2 piece hides the piece below — only the top piece counts for winning.
Each player gets 7 layer 2 pieces to spend strategically.

---

## Tech Stack
- **Pure HTML/CSS/JS** — single `index.html` file, no dependencies, no build step
- Open directly in browser OR serve with `python -m http.server`
- No backend, no database

---

## File Structure
```
connect4-layers/
├── index.html    # Board, styles, and game logic — all in one file
├── PLAN.md       # This file
├── README.md     # How to run
└── CLAUDE.md     # App builder process reference
```

---

## Features (Build Order)

1. **Board render** — Draw the 7x6 grid with empty cells
2. **Layer 1 dropping** — Click a column, piece falls to lowest empty row (gravity)
3. **Turn system** — Alternate between Player 1 (red) and Player 2 (yellow), show whose turn it is
4. **Win detection** — Check 4 in a row (H/V/diagonal) using topmost piece in each cell; show winner
5. **Layer 2 placement mode** — Toggle button to enter "layer 2 mode"; click any occupied cell to place a layer 2 piece on it
6. **Layer 2 counter** — Show each player's remaining layer 2 pieces (starts at 7 each)
7. **Visual styling** — Clear distinction between layer 1 and layer 2 pieces (e.g. layer 2 has a ring/border/shine); nice board colors
8. **New game button** — Reset everything to starting state

---

## Game Rules Summary
- **Layer 1:** Drop piece into column → falls to lowest empty row
- **Layer 2:** Spend one of your 7 special pieces → place on any cell that already has a layer 1 piece (yours or opponent's)
- **Win check:** For each cell, only the topmost piece counts. 4 topmost pieces of the same color in a row = win.
- **Covering:** Placing layer 2 on opponent's cell effectively steals it for win-checking purposes

---

## Unknowns / Decisions
- [ ] Draw condition? (board fills up with no winner) — show "Draw!" message
- [ ] What happens if a player runs out of layer 2 pieces? They just can't use layer 2 mode anymore.
- [ ] Animation for dropping pieces? Nice to have, add in polish pass if time allows.
