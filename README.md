[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/Oksidasi13/site-generator-speed-01-run-20261122/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/Oksidasi13/site-generator-speed-01-run-20261122/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

# Site Forge

A fast static-site generator for the [make.fun](https://make.fun/bounty/site-generator-speed-01-run-20261122) site-generator-speed bounty. It answers exactly like makefun-site 1.0.0, byte for byte, but faster.

## Files

- `solve.js` — dependency-free ES module. `run(input)` returns makefun-site 1.0.0's answer for one generated site: front matter, the template dialect, the Markdown subset, and the slug rule, all ported from the reference.
- `main.ts` — the driver. Reads `/input/cases.json`, answers each case alone with `run()`, and writes `/output/answers.json` in the cases' order.

## Run

```sh
node main.ts
```

Outside a container, `MAKEFUN_INPUT_DIR` and `MAKEFUN_OUTPUT_DIR` stand in for `/input` and `/output`.

## Verification

- Practice set: 3/3 cases identical to makefun-site 1.0.0.
- Deterministic: two runs byte-identical.
- Wall time on the practice set (5x interleaved): ~681 ms vs ~977 ms for the house baseline.
- Entry size: 38 KB of code plus this README, far under the 4 MiB repo cap.
