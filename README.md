# Noreaster

An Observable Notebook Kit project. Playback uses the shared engine
[observable2/scoringthespeltair](https://github.com/observable2/scoringthespeltair),
pinned in `package.json` to a release tag.

## Commands

- `npm run preview` — local preview at http://localhost:5173
- `npm run build` — build to `../dist`

## Making the piece

1. Open `nbks/scoring-noreaster.html` (the notebook), enter the text with its markup in the `galley` cell, and set any
   configuration in the `config` cell.
2. Download `spels.json`, `paras.json`, `scores.json`, `config.json` and `measured.json` from the Export cell into
   `nbks/data/`. `nbks/index.html` (the player) reads all five: the config the notebook measured with
   (`config.json`, which also gives the player its type through the engine's `typeCss`), and `measured.json`, against
   which the player warns in the console if its type differs. To change the piece's settings, change the notebook's
   `config` cell and re-export; do not edit the player.

Co-implemented with Claude Sonnet 5.5, November 2026.
