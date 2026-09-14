# Agora — Rebuild 2 mockup

**This is a mockup.** Nothing here analyses anything. Every screen is a script that does the same
thing at the same second every time.

Open [`index.html`](index.html). No server, no install, no build.

## What Agora is

Agora takes an article, a ruling, a paper or a strategy memo and does a lot of work on it before
anyone is allowed to speak. It pulls out the claims and the open questions. It works out who has
standing, splitting that into the people the outcome lands on and the people worth asking because
of what they know. Then it proposes a panel, and writes down each member's mandate in advance so
you can hold them to it.

Then the panel argues. Arguments carry their sources. Audience comments pile up and get clustered
into questions, and a question with enough weight behind it stops the panel until they deal with
it. When somebody changes their mind, what changed it gets recorded next to the change.

What comes out at the end is a map of the argument rather than a recording of it. Some of the
disagreements turn out to be about facts, and somebody could go and check. Most of them do not.

## The four screens

It plays through them on one clock. `❙❙ Hold pace` stops it, the scrub moves it, and the four
buttons jump straight to a screen. Paused, the columns scroll normally.

| | |
|---|---|
| **01 · Source** | A proposition goes in. Claims, questions and a forecast come out, standing is mapped, and five panellists are proposed with a mandate each. Nobody has spoken yet. |
| **02 · Deliberation** | The panel argues, and every contribution carries a claim, a source count and a confidence meter. At 14:11 thirty-seven audience comments cluster into one question and the panel stops to answer it. Maya then changes her position, and the record says who moved her. Minerals keep coming up and nobody on the panel knows anything about minerals, so the audience votes an economist in, 214 to 38. |
| **03 · Synthesis** | Where the argument got to. Three things everyone now agrees on, each traced back to the timestamps that produced it. Four that are still live. Two factual questions nobody has gone and answered, with whose job it is. |
| **04 · Taxonomy** | Each open dispute sorted by what could settle it: evidence, time, or nothing. |

## About the sample source

The subject is real. US pressure on Greenland's status, the 1951 defence agreement as amended at
Igaliku in 2004, Pituffik, the 2009 Self-Government Act — those are all real, and the arguments
are written to respect them.

The source excerpt is not real. It was written for the demo, and the page labels it
`SAMPLE SOURCE`. No news organisation published it. The six panellists are invented too, along
with their arguments, their citations, the comment counts and the vote. Nobody said any of this.

## Where it came from

Agora was one of six prototypes built in 48 hours at **Rebuild 2** in Helsinki, 30 August to
1 September 2026. The prototypes are collected at
[rebuild-digital/Rebuild-2-Prototypes](https://github.com/rebuild-digital/Rebuild-2-Prototypes).

Designed at Rebuild 2 by **Tim, Mikko, Ruggero and Lorenz**.

The original was a hosted artifact rather than a repo. What survived of it were seven DOM
snapshots taken at different points in the walkthrough, and those are what this was rebuilt from.
The layout, the copy, the palette and the sequence come from the snapshots. None of the code does.

## How it is put together

One HTML file. Inline CSS, vanilla JavaScript, nothing fetched over the network, nothing to build.

There was nothing here for a framework to do. It is a fixed script with no data and no interaction
beyond the transport controls, so a build step would only have added something else to go stale.
The repo is also an archive rather than a living project, and a single file will still open in ten
years.

The whole walkthrough is one number: a time `T` in seconds, and a function from `T` to a frame.
Nothing accumulates, so the scrub can land anywhere and the frame is still correct, and re-timing
the piece means changing numbers rather than logic.

The columns auto-scroll, but only far enough to bring the newest thing into view, and only while
it is playing. Once you pause it they stop moving on their own.

Inter and IBM Plex Mono are named first in the font stack with system fallbacks behind them,
rather than loaded. The page works offline and off a file path, and if you do not have those faces
installed it still reads fine.

## Licence

MIT — see [LICENSE](LICENSE).
