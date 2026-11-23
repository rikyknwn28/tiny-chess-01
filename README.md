# Tiny Chess Engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/rikyknwn28/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/rikyknwn28/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A compact chess engine for the make.fun tiny-chess-01 bounty (4,096-byte limit).

- 0x88 board, alpha-beta with PVS, null-move pruning, quiescence search
- Transposition table, MVV-LVA + killer + history move ordering
- PeSTO tapered piece-square evaluation (middlegame/endgame)
- Fixed 60,000-node budget per move (deterministic, no clock)
- Python 3.13 standard library only; no model calls; reads nothing at runtime

`main.py` is an LZMA-compressed payload with a tiny unpacker (the source is
decompressed and executed at startup). The engine talks to the env at
`MAKEFUN_ENV_URL` (`POST /game`, `POST /move`) and exits when all games end.

Run: `MAKEFUN_ENV_URL=http://127.0.0.1:PORT python3 main.py`

License: MIT.

---

<sub>Entered on [make.fun](https://make.fun/?ref=mrnt95zx&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
