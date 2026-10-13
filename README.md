# Classical & Adversarial Search Agent

Implementation of classical pathfinding and adversarial game-tree search algorithms on a grid world, for *Artificial Intelligence* (601.464), Johns Hopkins University.

## Part 1 — Classical Search
A robot (🤖) navigates a grid world with obstacles (⬛) to reach a goal (❤️), implemented and compared across three search strategies:
- **Breadth-First Search** — guarantees shortest path by number of moves (explores level-by-level).
- **Depth-First Search** — explores one branch fully before backtracking; not guaranteed shortest.
- **A\* Search** — optimal unit-cost path using straight-line distance as the heuristic.

Each algorithm visualises its frontier (🟨) and final path (🟩) directly on the grid, and is re-run with start/goal positions swapped to test directional sensitivity.

## Part 2 — Adversarial Search
Extends the world with a second, adversarial agent (👾 "bad robot") that tries to intercept the good robot before it reaches the goal (zap radius: 3×3 cells centred on itself). Modelled as a two-player zero-sum game:
- `max_value` / `min_value` — core **Minimax** recursion for the good robot vs. the adversary.
- Game terminates when either agent wins, or after 82 plies (41 moves each).

## Engineering constraints followed
- All functions documented with docstrings and covered by unit tests (≥3 conditions each).
- Functions kept under 20 lines, single-responsibility.
- No custom classes — pure functions over list-of-lists world representation.

## Repo contents
```
notebooks/submission.ipynb         Final compliant submission (BFS, DFS, A*, Minimax + unit tests)
notebooks/minimax_extended.ipynb   Extended/alternate working version of the adversarial search agent
```

## Tech stack
Python · standard library only (no ML frameworks — pure search/game-tree algorithms)

## Reproducing
```bash
jupyter notebook notebooks/submission.ipynb
# Kernel → Restart & Run All
```
