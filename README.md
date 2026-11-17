# tiny-chess-01 r13

A chess engine in 4,096 bytes of Python (packed `main.py`, 4,084 bytes).

Design: 64-square array with precomputed attack/ray tables, integer moves,
incremental material + piece-square evaluation, bishop pair, passed-pawn
bonus, PVS + transposition table + killers + history, quiescence with check
evasions, repetition scoring. Fixed node budget per move, no clock, no
randomness — the same position always gets the same move.

`engine.py` is the readable source; `main.py` is the packed entrypoint
produced by `makefun compress`. Played through the env at MAKEFUN_ENV_URL.
