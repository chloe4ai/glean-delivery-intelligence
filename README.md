# Glean · Delivery Intelligence

A single-file prototype built for a **Glean product management** conversation. It argues one
thing: that a search product sitting on top of every system a company uses is already
holding the raw material for a *proactive* intelligence layer, and that the hard problems in
building one are trust problems, not retrieval problems.

Open `index.html`. No build step, no dependencies, no backend.

```bash
python3 -m http.server 4792 --directory .
```

## The shift it proposes

Search is pull. Someone has to already suspect something is wrong, and know what to type.
Delivery Intelligence is push: every active project carries a live health score composed
from cross-system signals, so risk surfaces before it reaches a status report — twelve
projects across six teams, average health 71 and down six points this week, two below
threshold.

The persona switch at the top is the load-bearing claim. The same engine re-skins from
**Maya, VP Engineering** to **Diego, VP Revenue** — different projects, different signals,
identical machinery. If the engine only works for engineering delivery it is a feature; if
it generalizes across departments it is a platform, and the switch is there so a reader can
check rather than take it on faith.

## The four sections, and why each exists

**Portfolio health.** Projects sorted by risk, each clickable through to the evidence behind
its score. A health number nobody can open is a horoscope.

**The signal catalog.** Every connected system, how fresh it is, how much each raw signal
contributes to insight precision, and each signal's *measured* precision — with toggles that
recompute the scores live. This is the section the prototype is really built around: a
proactive insight pushed to a leader is only as good as its weakest signal, and surfacing
weight-plus-precision per signal is what makes the system auditable and what lets feedback
re-weight it over time. Push notifications without this are a trust liability.

**Agents draft, you approve.** Every insight can dispatch an agent to do the legwork, and
nothing ships on its own. The prototype takes a position on where the human sits in the loop
and stays there consistently, rather than leaving autonomy pleasantly vague.

**Search is still here.** It is just no longer the only way in, and every answer cites its
sources with follow-ups available. The proactive layer is additive; it does not ask anyone
to give up the behaviour they already have.

There is also a signal-to-noise control the user tunes themselves — the same instinct as the
precision bar in [glean-compass-v2](https://github.com/chloe4ai/glean-compass-v2): a
proactive system that cannot be turned down gets turned off.

## What it is not

A working system. Scores, signals and precision figures are authored to make the trust
architecture legible in conversation. What is on display is the product judgment — what has
to be true before a leader will act on an unrequested insight — not an implementation.

## Related

- [glean-compass-v2](https://github.com/chloe4ai/glean-compass-v2) — narrower cut of the same
  thesis: one detector, priority drift, with the precision tradeoff made explicit
- [glean-ei-fullstack](https://github.com/chloe4ai/glean-ei-fullstack) — the same ideas built
  as a real React + Express app, where the confidence recomputation actually runs server-side
