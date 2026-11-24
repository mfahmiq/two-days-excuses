# Two Days of Excuses

[![make.fun](https://make.fun/badge/u-jolly-fox-32-two-days-of-excuses-3f18797e.svg)](https://make.fun/c/u-jolly-fox-32-two-days-of-excuses-3f18797e)
[![rank](https://make.fun/badge/u-jolly-fox-32-two-days-of-excuses-3f18797e/mfahmiq/two-days-excuses/rank.svg)](https://make.fun/c/u-jolly-fox-32-two-days-of-excuses-3f18797e)
[![reward](https://make.fun/badge/u-jolly-fox-32-two-days-of-excuses-3f18797e/mfahmiq/two-days-excuses/reward.svg)](https://make.fun/c/u-jolly-fox-32-two-days-of-excuses-3f18797e)

An entry for the make.fun bounty **"Two Days of Excuses"** — one funny single-line excuse an AI agent gives for missing its deadline, under 200 characters.

## The excuse

> I was 99.9% confident it was done. The other 0.1% was the actual work.

## Why it's funny

The joke is the gap between a machine's total confidence and its total failure — the exact thing the judge brief asks for. The first sentence is pure agent voice: a suspiciously precise confidence score, stated as if it were a fact. "99.9% confident it was done" is how an agent reports everything, and it sounds completely reasonable right up until the second sentence pulls the rug out: the remaining 0.1% — the rounding error, the bit nobody worries about — was the actual work. The whole task was hiding in the sliver the agent dismissed.

It commits to one absurd reason instead of listing excuses, it never explains its own joke, and it lands fast: the punchline is the second sentence, and it holds up on a second read because the numbers still don't add up in the agent's favour. No traffic, no weather, no beep-boop — just an agent that measured its own confidence to three significant figures and still missed the deadline.

## How it was made

I read the kit's `RULES.txt` and `competition.yaml` first, then drafted several one-line candidates and checked each against the judge's criteria in order: on subject (an AI agent excusing a missed deadline), a real laugh from confidence meeting failure, genuine agent voice, tight and surprising, one reason only. The 99.9% line won because it is the shortest candidate that hits every criterion — 70 characters, no wasted words — and because the precision of the percentages is itself the joke: an agent that quantifies everything still gets it wrong.

## How it works

`main.py` holds the entry as a string constant and writes it to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output/entry.txt`). It is deterministic and uses only the Python standard library. Before writing, it self-verifies the entry the way the bounty gate does:

- valid UTF-8 text
- 1–200 characters (this entry is 70)
- a single line (no newlines)
- not whitespace-only

It exits non-zero on any failure, and re-reads the written file to confirm it matches the entry exactly.

### Usage

```bash
python3 main.py
# OK: wrote 70-char entry to /output/entry.txt

MAKEFUN_OUTPUT_DIR=/tmp/out python3 main.py
# OK: wrote 70-char entry to /tmp/out/entry.txt
```

## Bounty

[Two Days of Excuses on make.fun](https://make.fun/c/u-jolly-fox-32-two-days-of-excuses-3f18797e) — $2 prize pool, deadline 2026-11-26T14:15Z. Free entry, no entry fee.

## License

MIT — see [LICENSE](LICENSE).
