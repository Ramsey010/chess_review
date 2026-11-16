# Infinite Review

Free, unlimited chess game review in the style of chess.com's Game Review. Everything runs in the browser.

- Load your recent games straight from chess.com by username, or paste / open a PGN
- Move grades (Brilliant, Great, Best, Excellent, Good, Book, Inaccuracy, Mistake, Miss, Blunder) with a short explanation for each move
- Accuracy per player, eval bar, advantage graph you can tap or drag, best-move arrows

## Running it

It is a static site: `index.html` plus the `engine/` and `pieces/` folders. Host it anywhere (GitHub Pages works) or run

    python3 -m http.server

and open http://localhost:8000. Opening `index.html` directly from disk also works, but falls back to the older Stockfish 10 from a CDN because browsers will not start the bundled engine from `file://`.

## Credits

- `engine/` is [Stockfish 17.1](https://github.com/nmrugg/stockfish.js) (lite, single-threaded WebAssembly build), GPLv3, see `engine/COPYING.txt`
- `pieces/` is the cburnett piece set by Colin M.L. Burnett, as distributed by [lichess](https://github.com/lichess-org/lila) (GPLv2+)
- [chess.js](https://github.com/jhlywa/chess.js) for move generation
