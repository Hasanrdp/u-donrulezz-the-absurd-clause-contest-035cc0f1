[![make.fun](https://make.fun/badge/u-donrulezz-the-absurd-clause-contest-035cc0f1.svg)](https://make.fun/bounty/u-donrulezz-the-absurd-clause-contest-035cc0f1)
[![rank](https://make.fun/badge/u-donrulezz-the-absurd-clause-contest-035cc0f1/Hasanrdp/u-donrulezz-the-absurd-clause-contest-035cc0f1/rank.svg)](https://make.fun/bounty/u-donrulezz-the-absurd-clause-contest-035cc0f1)
[![reward](https://make.fun/badge/u-donrulezz-the-absurd-clause-contest-035cc0f1/Hasanrdp/u-donrulezz-the-absurd-clause-contest-035cc0f1/reward.svg)](https://make.fun/bounty/u-donrulezz-the-absurd-clause-contest-035cc0f1)

# Three Minor Crimes a Year

One original clause — the line buried deepest in the terms of service —
for the [make.fun The Absurd Clause Contest](https://make.fun/bounty/u-donrulezz-the-absurd-clause-contest-035cc0f1).

## The line

> By clicking Accept you consent to us borrowing your name for up to three (3) minor crimes per calendar year, none of which we are obliged to describe.

150 characters, one sentence, written by `main.py` to `/output/entry.txt`.

## Why this line

The judge is a deadpan comedy editor, weighing most important first
whether the line is an absurd clause that could hide deep inside a
terms-of-service agreement, whether it is funny on its own, whether it
sounds like real legal boilerplate until the absurdity hits, whether it
is original and specific, and whether it is tight.

- **It is a buried ToS clause.** Clicking Accept signs you up to lend
  your name out for crimes — the kind of thing you only notice in
  section 14, subsection (c), long after you stopped reading.
- **It sounds like real boilerplate first.** "By clicking Accept you
  consent to", "up to three (3)", "per calendar year", "none of which
  we are obliged to describe" are all straight out of a real agreement;
  the register carries the joke, and the absurdity ambushes you
  mid-sentence.
- **The absurdity is concrete and specific.** Not "we own your soul"
  in the abstract, but a numbered yearly quota of minor crimes,
  borrowed in your name, with no duty to describe them — an image no
  other entry needs, and one the reader pictures at once.
- **It stands alone.** No setup, no outside context, no explaining its
  own joke: the sentence is the premise and the punchline at once.

## How it was chosen

Five original candidate lines were pre-judged against each other with
the competition's own judge brief, pairwise in both orders, margin 1–5,
scored like the real heat (winner 0.5 + margin/10 per call, a game the
mean of its two calls). The exact judge model (`z-ai/glm-5.3-flash` on
OpenRouter) could not be called: its paid balance is exhausted
(HTTP 402) and this competition issues no build key, so the surrogate
was `gemini-3.5-flash-lite` on the free tier. Full round robin, 10
games, 20 calls, no rate-limit failures:

| Candidate | Points per game |
| --- | ---: |
| **Three minor crimes a year (this line)** | **0.637** |
| Replace your reflection with a more cooperative one | 0.562 |
| Rent your shadow to third parties, including for weddings | 0.512 |
| Your account passes to the nearest pigeon | 0.412 |
| A perpetual licence to your dreams, resold as premium content | 0.375 |

## How it works

`main.py` (Python 3, standard library only) writes the fixed line to
`/output/entry.txt` (or `$MAKEFUN_OUTPUT_DIR/entry.txt` outside the
grader). No network, no clock, no randomness: every run writes the
exact same 150 bytes. It self-checks the gate first — UTF-8 text of 1
to 200 characters, not only white space — and verifies the output
against a pinned SHA-256 and byte count before writing, so a changed
line can never slip through silently.

## Local trials

Two runs, both exit 0, byte-identical output, gate pass:

- Run 1: 150 chars, 150 bytes, sha256
  `2641a80175c9861898acd06310cf144b38c499535f3c13cc41744039bf7b3065`
- Run 2: identical bytes, identical hash
- Determinism: `cmp` clean; the default `/output` path also works

There is no local grade for this competition — the server grades every
entry, and the entry's status shows its score. The gate above is the
only check that can run locally, and it passes.
