# Noreaster

An Observable Notebook Kit project. Playback uses the shared engine
[observable2/scoringthespeltair](https://github.com/observable2/scoringthespeltair),
pinned in `package.json` to a release tag.

## Commands

- `npm run preview`: local preview at http://localhost:5173
- `npm run build`: build to `../dist`

## Making the piece

1. Open `nbks/scoring-noreaster.html` (the notebook), enter the text with
   its markup in the `galley` cell, and set any configuration in the
   `config` cell.
2. Save `spels.json`, `paras.json`, `scores.json`, `config.json` and
   `measured.json` from the Export cell into `nbks/data/`. The player
   (`nbks/index.html`) reads all five. The Export cell also writes
   `spels-raw.json`, a copy of `spels.json` as measured: keep it if you
   edit `spels.json` by hand (`diff spels-raw.json spels.json`). `config.json` is the config the
   notebook measured with; it also gives the player its type, through the
   engine's `typeCss`. `measured.json` lets the player warn in the console
   if its type differs from the type measured. To change the piece's
   settings, change the notebook's `config` cell and export again; do not
   edit the player.

Co-implemented with Claude Sonnet 5.5, November 2026.
