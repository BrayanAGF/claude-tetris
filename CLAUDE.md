# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project constraints

- Vanilla HTML5 Canvas + CSS + JS. No dependencies, no `package.json`, no bundler, no transpiler — don't add any. `game.js` is loaded with a plain `<script>` tag (not a module).
- No build or tests. To try changes, serve the folder statically (e.g. `python -m http.server 8000`) and open `http://localhost:8000`.

## Gotchas

- `COLS × BLOCK` and `ROWS × BLOCK` in `game.js` must match the `width`/`height` of `<canvas id="board">` in `index.html` (currently 300×600). Change both together.
- Cell values in `PIECES` and `board` are the piece type index (1–8), which doubles as the index into `COLORS`; `0` means empty. Keep the three arrays aligned.
- Controls are listed in three places: the `keydown` handler in `game.js`, the controls panel in `index.html`, and the table in `README.md`. Update all of them together.

## Conventions

- Write everything in Spanish: UI text, README, new code comments, and commit messages.
- README.md documents mechanics, scoring, level speed, controls, functions, and tunable constants in detail. Update it whenever a change affects any of these.
