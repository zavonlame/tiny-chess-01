# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/zavonlame/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/zavonlame/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A tiny Python chess engine squeezed into 4 KB. It searches with alpha-beta and iterative deepening over a 0x88 board, capped at a fixed 100,000 nodes per move, with quiescence search, a transposition table, MVV-LVA plus killer move ordering, null-move pruning, and late-move reductions. The evaluation uses material plus precomputed piece-square tables (a linear pawn-advance term, so the engine develops pieces instead of shoving pawns). In a local trial-0 run against the house sunfish gauntlet it scored Elo 1,191 (2 wins, 1 draw, 3 losses), above the 1,154 practice floor. The readable source (engine.py) is packed with the kit's own makefun compress into the 4,096-byte main.py. Every move is deterministic: the same position always gets the same move, because the search runs to a fixed node budget and never uses a clock or unseeded randomness.

## Run it

```sh
makefun grade-local --kit . --bot https://github.com/zavonlame/tiny-chess-01 --driver docker
```

---

Entered on [make.fun](https://make.fun/?ref=ye09dzcs&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards
