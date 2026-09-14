# Agora — Rebuild 2 mockup

**This is a visual mockup. It is not a working system.** Nothing is analysed, retrieved or
generated. Every screen is a scripted animation that does the same thing at the same second every
time.

Open [`index.html`](index.html). No server, no install, no build.

## What Agora is

*A living map of disagreement.*

Agora takes any article, ruling, paper or strategy memo and, before anyone speaks, extracts its
claims and open questions, maps who has standing — those affected by the outcome and those
invited for expertise — then proposes a panel of constructed personas, each with an explicit
mandate. In the deliberation that follows, every argument carries its sources, audience comments
cluster into questions that pause the panel, and when a participant changes position the revision
is recorded with the reason.

The output is not the transcript. It is a map of what the disagreement actually is.

## The four screens

The page plays through them on one clock. `❙❙ Hold pace` stops it, the scrub moves it, and the
four buttons jump straight to a screen.

| | |
|---|---|
| **01 · Source** | A proposition is pasted. Claims, questions and forecasts are extracted, standing is split into *affected by outcome* and *invited for expertise*, and a panel of five is proposed — each with a one-line mandate. Nobody has spoken yet. |
| **02 · Deliberation** | The panel argues. Every contribution carries a claim, a source count and a strength meter. At 14:11 thirty-seven audience comments cluster into a question and **the panel is paused** to answer it. Maya then changes position and the revision is recorded with who moved her. A **perspective gap** is detected — minerals are being discussed and nobody represents resource economics — and the audience votes a new participant in, 214 to 38. |
| **03 · Synthesis** | *"The output is the map, not the transcript."* Three areas of agreement, each traced back to the timestamps that produced it. Four disagreements that remain fundamental. Two factual questions still open, with who owes the answer. |
| **04 · Taxonomy** | Every open dispute classified by what could resolve it: **factual** (evidence settles it), **forecast** (time settles it), **value** and **interest conflict** (nothing settles them). |

## About the sample source

The subject is a real and live dispute — US pressure on Greenland's status, the 1951 defence
agreement as amended at Igaliku in 2004, Pituffik, the 2009 Self-Government Act. Those things are
real and the argument is written to respect them.

**Everything else is invented.** The source excerpt is composed and labelled `SAMPLE SOURCE` on
the page; it is not a report by any news organisation. The six panellists are constructed
personas with explicit mandates, not simulations of real individuals. Their arguments, their
citations, the comment counts and the vote are all fabricated for the mockup. Nothing here is a
record of anything anyone said.

## Where it came from

Agora was one of six prototypes built in 48 hours at **Rebuild 2** in Helsinki, 30 August –
1 September 2026. The prototypes are collected at
[rebuild-digital/Rebuild-2-Prototypes](https://github.com/rebuild-digital/Rebuild-2-Prototypes).

Designed at Rebuild 2 by **Tim, Mikko, Ruggero and Lorenz**.

This repo rebuilds the prototype as a single standalone page. The original was published as a
hosted artifact; what survived of it were seven DOM snapshots taken at different moments of the
walkthrough. Those were the reference — the layout, the copy, the palette and the sequence come
from them, the code does not.

## Stack

One self-contained HTML file. Inline CSS, vanilla JavaScript, no dependencies and no build step.

A framework would have bought a `node_modules` and a lockfile to go stale in exchange for
nothing: this is a fixed-script walkthrough with no data and no interaction beyond the transport
controls. A single file also stays runnable years from now, which matters more for an archived
artefact than for a product.

Three things worth naming:

- **One clock.** The whole walkthrough is a single time `T` in authored seconds and a pure
  function from `T` to a frame. Nothing accumulates state, so the scrub can jump anywhere and the
  frame is always right. Re-timing it means editing numbers, not code.
- **Panes scroll, and stop fighting you.** Each column auto-scrolls only far enough to bring the
  newest revealed element into view, and only while playing — so the top of a screen stays
  readable until it has to move, and a paused viewer can scroll wherever they like.
- **Fonts are named, not fetched.** Inter and IBM Plex Mono are named first in the stack with
  system fallbacks behind them. The page loads nothing over the network, so it works offline and
  from a file path; where those faces are not installed it falls back and stays legible.

## Licence

MIT — see [LICENSE](LICENSE).
