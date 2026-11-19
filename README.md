# tiny-chess-01 entry

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Whenruq/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Whenruq/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python (packed with
`makefun compress` from a readable source), built for make.fun's
"Build the strongest chess engine in 4 KB of Python" bounty.

- 120-square string board, rotated each move so the side to move is
  always the uppercase army at the bottom.
- Iterative deepening under a fixed node budget (no clock, so replays
  match), alpha-beta with principal-variation search, transposition
  table, quiescence over captures, null-move pruning, late-move
  reductions, check extensions, killer moves, MVV-LVA ordering.
- Evaluation: material, piece-square tables with a tapered king,
  bishop pair, passed-pawn bonuses.

It plays the gauntlet through the env at `MAKEFUN_ENV_URL`, choosing
each root move among the legal moves the env serves.
