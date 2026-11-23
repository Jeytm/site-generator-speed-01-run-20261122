# Build a static site faster — site-generator-speed-01-run-20261122

![Competition](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)
![Rank](https://make.fun/badge/site-generator-speed-01-run-20261122/Jeytm/site-generator-speed-01-run-20261122/rank.svg)
![Reward](https://make.fun/badge/site-generator-speed-01-run-20261122/Jeytm/site-generator-speed-01-run-20261122/reward.svg)

Entry for the [make.fun bounty](https://make.fun/bounty/site-generator-speed-01-run-20261122): a faster drop-in for makefun-site 1.0.0.

`solve.js` is a dependency-free ES module whose `run(input)` returns, byte for byte, the output tree makefun-site 1.0.0's `build` returns for a site: every page's `index.html`, the index and tag pages, `build-report.txt` and each static file. It reimplements makefun-site's own front matter, template dialect, Markdown subset, slug rule and report — streaming block rendering, a single-scan inline renderer, cached slugs and dates, allocation-light template walks. `main.ts` is the driver the harness runs: it reads every case from `/input/cases.json`, answers each with `run`, and writes `/output/answers.json`.

Verified on the practice set: 3/3 cases pass against the reference expected output, deterministic across runs (identical `answers.json`, sha256 `25980928b145f54712027939364a64c277098bc4528a2d524e0bc27a0275fb03`). On this machine the entry runs the practice set in ~0.9 s vs ~1.5 s for the house baseline.
