# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/mattxzte/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/mattxzte/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A compact chess engine in 4 KB of Python: 0x88 board, negamax alpha-beta with iterative deepening on a fixed node budget, quiescence search, a transposition table, MVV-LVA/killer/history move ordering, and a piece-square-table evaluation with bishop-pair, doubled- and passed-pawn terms. It plays the make.fun trial protocol — deterministic, stdlib only, no wall clock, no model calls.

## Engine

The search is negamax with alpha-beta windows and iterative deepening: each root move is probed with a zero window first and re-searched wide only when it improves, and late quiet moves get a reduced-depth look before a full re-search. A direct-mapped transposition table stores mate-adjusted scores, null-move pruning skips a turn when the position is comfortably ahead, and the quiescence search extends captures, promotions, and check replies with delta pruning so the horizon does not hide a hanging piece. Evaluation combines material and piece-square tables with a bishop-pair bonus, doubled-pawn penalties, flat passed-pawn bonuses, and an endgame king table once the phase thins out. Every move is decided on a fixed budget of 125,000 search nodes — no clock, no randomness — so a trial replays move for move, and the board is keyed with deterministic Zobrist hashes seeded from a fixed constant.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8000 python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=nv10mx49&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
