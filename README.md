# The Great Trapeze

A browser-based circus trapeze arcade game. Time your release, fly bar to bar, and let the clowns catch you if you fall.

**▶ Play:** https://elmygl.github.io/the-great-trapeze/

---

## An Experiment in Vibe Coding

This game was built entirely through conversational "vibe coding" — describing what I wanted in plain language to an AI collaborator (Claude) and iterating on the results, rather than writing the code by hand.

The playable core came together quickly. The real work — and the interesting part of the experiment — was the long tail of iterative refinement: getting the swing physics to *feel* right, balancing the difficulty curve, and tuning the game so every jump stays fair.

## How to Play

- **Space** — release from the trapeze at the right moment to fly to the next bar
- **R** — restart
- **M** — toggle music

She auto-catches the next bar if your timing lands. Miss, and a trio of clowns with a bouncy blanket will catch you — but only **three times** per run. Climb the ranks from **Novice** to **Master Acrobat**.

## Development

**Time:** Approximately 3 hours of hands-on iteration in a single session, distributed roughly as:

| Phase | Time | Work |
|---|---|---|
| Initial build | ~30 min | Core swing/release/catch loop, canvas rendering, circus-poster styling |
| Physics tuning | ~75 min | Swing height & speed, flight distance, release consistency, spacing — the largest share |
| Features & content | ~50 min | Trampoline/clown-catch mechanic, performer parade, ringmaster, embedded soundtrack |
| Polish & presentation | ~25 min | Title banner, clown faces, rank system, star-rated scorecard |

**Process:** Roughly 25–30 distinct rounds of iteration, ranging from one-line tweaks (text size, colors) to substantial features (a clown-held safety net with a 3-catch limit, a parading circus troupe, an embedded MIDI soundtrack, and a star-rated scorecard). Each physics change was validated through 30+ simulation runs that confirmed every jump remained catchable across the full difficulty curve before it shipped.

*(Time and step counts are honest estimates from reviewing the build session, not precise measurements.)*

## Stack

A single self-contained HTML file — vanilla JavaScript, HTML5 Canvas, and Web Audio synthesis, with the soundtrack embedded as compressed note data. No external dependencies, no build step. Just open the file.

---

© 2026 Elmer Yglesias · Ver. 1.0
