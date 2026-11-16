# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/mattxzte/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/mattxzte/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A compact chess engine in 4 KB of Python: 0x88 board, negamax alpha-beta with iterative deepening on a fixed node budget, quiescence search, a transposition table, MVV-LVA/killer/history move ordering, and a piece-square-table evaluation with bishop-pair, doubled- and passed-pawn terms. It plays the make.fun trial protocol — deterministic, stdlib only, no wall clock, no model calls.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8000 python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=nv10mx49&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
