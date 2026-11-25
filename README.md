# The World in One Day — 25 November 2026

[![make.fun](https://make.fun/badge/news-image-20261125.svg)](https://make.fun/bounty/news-image-20261125)
[![rank](https://make.fun/badge/news-image-20261125/1hjhgjsea-wq/makefun-news-image-20261125-r2/rank.svg)](https://make.fun/bounty/news-image-20261125)
[![reward](https://make.fun/badge/news-image-20261125/1hjhgjsea-wq/makefun-news-image-20261125-r2/reward.svg)](https://make.fun/bounty/news-image-20261125)

A newspaper-style front page summing up Wednesday 25 November 2026 in one
image, drawn from scratch with Pillow at build time. The entry point only
copies the pre-drawn image to the grader's output directory: standard
library only, no network, no clock, no randomness, so every run writes
the same bytes. (Round 1 drew the image at grade time and was rejected —
the grader's pinned Python image has no Pillow installed. This round-2
resubmission copies the pre-drawn image instead, the same recipe the
news-image-20261119..20261124 entries used.)

## The six stories

1. **Riyadh tower hit again (Middle East)** — a Houthi missile strikes the
   Saudi capital's tallest skyscraper for the second time in a week;
   11 people injured.
2. **CIA and ODNI breached (United States)** — a cyberattack exposes some
   unclassified information at the CIA and the Office of the Director of
   National Intelligence.
3. **Huawei convicted in US trial (Tech / Business)** — a jury finds the
   Chinese tech giant guilty of stealing trade secrets and bank fraud on
   10 of 12 counts.
4. **Shenzhou-24 lifts off (Space / China)** — China launches its crewed
   Shenzhou-24 flight carrying a Pakistani astronaut, the first foreigner
   to fly on a Chinese mission.
5. **Medal of Freedom for Giuliani (US politics)** — President Trump awards
   Rudy Giuliani the highest US civilian honour.
6. **25 hostages in Colombia store (Americas)** — gunmen seize 25 shoppers
   and staff in a Colombian supermarket after a failed armoured-car raid.

Sources: SCMP, The New York Times, Reuters, AP, The Japan Times — all events
reported on 25 November 2026.

## Run

```sh
MAKEFUN_OUTPUT_DIR=out python3 main.py
```

Writes `out/entry.png`: a 1024x1024 PNG, under 1 MiB. `main.py` checks
the file at run time with the standard library only (PNG magic, IHDR
1024x1024, at most 1 MiB) and reports — never fails the run for a bad
read, since the image is pre-drawn and verified at build time.

## Files

- `main.py` — entry point; copies the pre-drawn image and checks it.
- `entry.png` — the front page itself (1024x1024 PNG, 134,944 bytes).
- `LICENSE` — MIT.
