# Chess vs Bot

A single-file browser chess game with a JavaScript chess engine. Play against an AI opponent at four difficulty levels, with opening book, post-game PGN export, and Lichess analysis integration.

## Features

- **Full chess rules** — castling, en passant, promotion, all draw conditions (50-move, threefold repetition, insufficient material, stalemate)
- **Four difficulty levels** — Easy (~1100), Medium (~1500), Hard (~1800), Expert (~2100)
- **Bot personalities** — Balanced, Aggressive, Defensive, or Positional play styles
- **Choose your color** — play as White, Black, or Random at the start of each game
- **Engine optimizations** — minimax with alpha-beta pruning, quiescence search, transposition table, iterative deepening with time budgets, opening book
- **Move history navigation** — click any move to jump back, use arrow keys to step through
- **PGN export** — download your game or open it in Lichess for free Stockfish analysis
- **Right-click annotations** — multiple highlights and arrows in four colors (red / green / yellow / blue via Shift/Ctrl/Alt), with chess.com-style L-shaped knight arrows
- **Pre-moves** — queue your move during the bot's turn
- **Sound effects, eval bar, captured pieces display, takebacks, draw offers, resignation**
- **Settings persist** between sessions via localStorage

## How to run

It's a single HTML file. Either:

1. **Just open `index.html` in your browser** — no build step, no server needed.
2. Or visit the GitHub Pages site (if enabled): `https://christos-michael.github.io/Chess-Bot/`

## Keyboard shortcuts

Press `?` in-game to see all shortcuts, or click the help button next to the title.

| Key | Action |
|-----|--------|
| F | Flip board |
| N | New game |
| ← / → | Navigate moves |
| Home / End | Jump to start / current |
| Esc | Cancel selection |
| ? | Show shortcuts help |

## Notes on bot strength

The Elo ratings shown next to each difficulty are educated estimates based on standard chess engine literature (depth 3 minimax with alpha-beta and quiescence search ≈ 1500 Elo, each additional ply ≈ +200-300 Elo). They are NOT calibrated against real engines like Stockfish — actual playing strength could be ±200 Elo from the displayed numbers. The relative ordering is reliable: each difficulty is meaningfully stronger than the one below it.

## Credits

- Chess piece graphics by **Cburnett**, from Wikimedia Commons, licensed under [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).
- Built with vanilla JavaScript — no frameworks or external libraries.
- Lichess integration uses the public `/paste` endpoint of [lichess.org](https://lichess.org).

## License

MIT — see [LICENSE](LICENSE).
