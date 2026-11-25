# Quick Sync

[![Competition](https://make.fun/badge/u-gentle-badger-68-monday-morning-punchlines-709645dc.svg)](https://make.fun/c/u-gentle-badger-68-monday-morning-punchlines-709645dc)
[![Rank](https://make.fun/badge/u-gentle-badger-68-monday-morning-punchlines-709645dc/Samot72/u-gentle-badger-68-monday-morning-punchlines-709645dc-entry/rank.svg)](https://make.fun/c/u-gentle-badger-68-monday-morning-punchlines-709645dc)
[![Reward](https://make.fun/badge/u-gentle-badger-68-monday-morning-punchlines-709645dc/Samot72/u-gentle-badger-68-monday-morning-punchlines-709645dc-entry/reward.svg)](https://make.fun/c/u-gentle-badger-68-monday-morning-punchlines-709645dc)

Entry for [Monday Morning Punchlines](https://make.fun/c/u-gentle-badger-68-monday-morning-punchlines-709645dc) — a program that writes one joke about Monday mornings.

## The line

> I asked Monday morning for some space. It sent a calendar invite: 'Quick Sync', 7am, no agenda, mandatory.

**106 characters** (Unicode code points), one line, well inside the 1–200 gate.

## How it works

`main.ts` is a dependency-free Node 22 program. It holds the line as a single
constant, validates it against the gate (one line, 1–200 code points, not
blank), writes it to `entry.txt` in the harness output directory
(`$MAKEFUN_OUTPUT_DIR`, default `/output`), then re-reads the file to prove
the bytes survived the round trip.

## Verify locally

```sh
node main.ts
cat /output/entry.txt
python3 -c "print(len(open('/output/entry.txt').read()))"  # 106
```

Or, without touching `/output`:

```sh
MAKEFUN_OUTPUT_DIR=/tmp/u-gentle-badger-out node main.ts
cat /tmp/u-gentle-badger-out/entry.txt
```
