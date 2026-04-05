# Project Retrospective — Software Quality Handbook

*Written by Antonin Miranda, with input from Kylian Tranchet and Hugo Denis.*

---

## What Went Well

**The topic split worked.** Dividing the three handbook sections by owner meant each person could focus and go deep on their subject without blocking anyone else. The parallel work on separate branches avoided most merge conflicts.

**The Git workflow held up.** We followed trunk-based development throughout — short branches, pull requests, no direct commits to main. Having the branching strategy decided upfront meant we didn't have to debate it mid-project.

**Pull request reviews were useful.** Beyond just approving, the reviews caught a few inconsistencies in tone and formatting early, before they spread across the whole document. It was more useful than we expected.

---

## What Didn't Work

**We underestimated the research phase.** Finding 5 quality sources per topic that were experience-based rather than purely theoretical took longer than planned. We assumed it would be quick and it wasn't.

**Coordination on shared files was awkward.** When multiple people needed to touch `handbook/index.md` (for the contributions table, the intro, links), we had to be careful about timing to avoid conflicts. A clearer ownership rule for shared files would have helped.

**The formatting pass came too late.** Kylian's formatting review was planned as the final step, but some inconsistencies had already spread through several files by then. Catching formatting issues earlier — or agreeing on a stricter style guide at the start — would have saved time.

---

## What We'd Do Differently Next Time

- **Set a style guide on day one.** Even a short one — heading levels, bullet point style, how to cite sources. It would have made the formatting pass almost unnecessary.
- **Time-box the research phase.** Give it a fixed slot and move on, rather than letting it expand.
- **Define ownership of shared files more explicitly** in the project plan, to avoid coordination overhead mid-project.
- **Start reviews earlier.** Rather than waiting for a section to be fully written, reviewing a draft earlier would have caught structural issues before they were hard to change.

---

## Lessons Learned

Working with a shared Git repository on a documentation project is not that different from a code project — the same problems appear: merge conflicts, inconsistent style, unclear ownership. The practices we documented in the handbook (clear task ownership, short branches, early feedback) are just as applicable to writing as they are to coding. In some ways, going through the process ourselves while writing about it made the content more grounded.
