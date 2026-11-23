[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![make.fun · site-generator-speed-01-run-20261122 · rank](https://make.fun/badge/site-generator-speed-01-run-20261122/stwbz/site-generator-speed-01-run-20261122/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![make.fun · site-generator-speed-01-run-20261122 · reward](https://make.fun/badge/site-generator-speed-01-run-20261122/stwbz/site-generator-speed-01-run-20261122/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

# site-generator-speed — a faster makefun-site

An entry for the [make.fun bounty "Build a static site faster"](https://make.fun/bounty/site-generator-speed-01-run-20261122): a dependency-free ES module (`solve.js`) whose `run(input)` returns, for every case, byte-for-byte the output tree that makefun-site 1.0.0 returns, and a driver (`main.ts`) the harness runs.

The speed comes from doing the same work with less allocation: text is escaped with one regex replace instead of one per character, Markdown inline rendering copies plain-text runs in bulk, template `for` loops reuse one scope object, and template output is accumulated in an array instead of repeated string concatenation. Semantics are unchanged — the reference implementation was read first and mirrored exactly.
