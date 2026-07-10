# Product Teardown
## Why the Manual TE-to-Course Alignment Process Failed

*Reconstructed for portfolio purposes from the delivered Innovation Week project (TE-to-Course Alignment Accelerator).*

---

## What's being torn down

Before the Accelerator existed, "alignment" meant a person opening a Spanish-language Teacher Edition, reading it lesson by lesson, and manually typing what they found into a spreadsheet. This teardown isn't about that person's effort — it's about why the *system* around them guaranteed the work would stay slow, no matter how good they were at it.

## The surface symptom

Every unit took roughly 60 hours to align. Framed this way, it looks like a throughput problem: too much manual reading, not enough automation. That framing suggests an obvious fix — speed up the typing, or add more people.

That fix would have failed. It treats the symptom, not the cause.

## The actual root cause

The system meant to make this fast — the CAT tracker — already existed. It just didn't work for this program. It had been **cloned from the ELA (English Language Arts) product** and never adapted for what SLA (Spanish Language Arts / *Emerger Juntos*) actually needed to track: biliteracy-building components, cross-linguistic connections, dictation printables, and other non-transferable, SLA-specific skills.

This is the distinction that matters: the team wasn't missing a tool. They had a tool that was **structurally wrong for the content it was supposed to represent.** A cloned system carries its parent's assumptions with it — and ELA's assumptions about what a "component" is don't hold for a dual-literacy program built around two languages moving together.

## Why this made the problem worse than "slow"

A tool that's merely slow degrades gracefully — you get less output per hour, but what you get is trustworthy. A tool that's *structurally wrong* is more dangerous, because it doesn't fail loudly. It produces output that looks complete and isn't.

That's exactly what happened here. Because the CAT tracker couldn't be trusted to reflect SLA's real components, every downstream team had to independently re-verify it:

- **Instructional Design** re-extracted from the TE directly, every time, because the tracker wasn't a reliable source
- **Course Build** couldn't build against the CAT without separately checking it against the TE
- **CAD** received verification requests that were inconsistently formatted, because there was no shared, trusted format to request against

None of these teams were being inefficient. Each one was rationally responding to a tool they couldn't trust. **The 60 hours wasn't the cost of doing the alignment work — it was the cost of doing it once per team, per unit, forever**, because no single output was ever treated as final.

## Why it never got better on its own

A normal inefficient process improves with repetition — people get faster, they build shortcuts, muscle memory kicks in. This one didn't, and the reason is structural: **the output was never reusable.** Each unit's manual extraction lived in that unit's spreadsheet and nowhere else. There was no compounding. Unit 40 took as long as unit 1.

That's the signature of a process problem masquerading as a volume problem. No amount of individual speed fixes a system with no memory.

## What a symptom-level fix would have missed

If the team had simply hired more people, or pushed for faster manual entry, the underlying issue — a tracker that didn't reflect the actual content model — would have stayed in place. Verification burden across three teams would have continued. New instructional decisions (like adding dictation printables) still couldn't be systematically rolled out, because the system of record still couldn't represent them.

Speed was never the constraint. **Trust in the system of record was.**

## What the Accelerator actually fixed

The AI-assisted workflow didn't just make extraction faster — it produced a **verified, reusable, QC-ready output** for the first time, which is a different kind of fix than "do the same thing quicker." And critically, the rollout plan sequenced a fix to the CAT tracker itself *after* the extraction workflow was proven — using the newly verified output as the audit source to correct the tracker's SLA blind spots. The teardown's root cause and the project's actual fix point at the same place.

---

## Why this teardown belongs in a TPM portfolio

Diagnosing *why* something is slow, and correctly distinguishing a throughput problem from a structural-trust problem, is the harder and more valuable half of product work — the half that determines whether a fix actually holds or just moves the same cost somewhere else. This is the piece of the Accelerator story that shows that judgment most directly.
