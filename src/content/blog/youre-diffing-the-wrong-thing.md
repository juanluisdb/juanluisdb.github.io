---
title: "You're Diffing the Wrong Thing"
description: "Teams preserve the diff and lose the reasoning that made the diff make sense."
pubDate: 2026-04-01
hero: "diff-review"
coverImage: "/images/blog/youre-diffing-the-wrong-thing-cover.png"
coverAlt: "A stylized screenshot of a diff where business context changes the implementation."
---

Code used to be the expensive part of software. Now teams can generate plenty of it. The slower part is carrying the reason for the change all the way into implementation.

We still treat the diff as the change, even though a lot of the change happened before the diff existed. The PRD changed the shape of the feature. The RFC discussion killed the first design. Support clarified where users actually get stuck. Customer success explained why a weird edge case is carrying real revenue weight. By the time the code lands in Git, a lot of the important work has already happened somewhere else, and nothing pulled it in.

Humans can work around that split. They ask around, reconstruct intent from scattered artifacts, and fill gaps with context they already have. Agents change the stakes because they cannot do that second part. A codebase can show an agent logic; it cannot show intent with the same fidelity. It does not tell the model why a simpler implementation was rejected, why an awkward behavior is load-bearing, or why one customer workflow matters more than ten cleaner abstractions. Without that reasoning, the output is often plausible and still wrong.

This is more than a documentation problem because the missing reasoning is often part of the implementation surface itself. Sometimes it shows up as a design constraint buried in an RFC thread, or an architecture note that never made it into the spec. Sometimes it is product reasoning, customer context, the argument that made the approved plan look the way it does. Either way, it keeps shaping the implementation after coding starts.

Spec-driven development gets part of the way there. The spec is useful, but the reasoning around the spec matters too. Teams are pretty good at preserving the clean artifact and much worse at preserving the argument that produced it. An approved plan survives. The useful mess around it usually doesn't.

Once that reasoning keeps doing work after implementation starts, it is no longer commentary. It is part of the change. If people keep going back to the RFC thread, the PRD, or the support recap during implementation, review, and follow-up fixes, part of the implementation surface is still missing from Git.

We are still preserving the diff and losing the work that made the diff make sense.
