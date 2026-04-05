# Code reviews
## Before you hit Approve — a checklist

The problem with code reviews is that it's easy to feel like you've done one without actually doing one. You scroll through the diff, nothing jumps out, you click Approve. That's not a review, that's just adding your name to it.

Having a concrete list to work from helps. Here's what to actually look for:

**As the reviewer:**
- [ ] Do you understand what this PR is actually trying to do? (If the description doesn't tell you, ask — don't guess)
- [ ] Does the code do what the description says, or is there a gap?
- [ ] What happens at the edges — null inputs, empty arrays, values that are technically valid but weird?
- [ ] Can you follow the logic without the author's help?
- [ ] New functions — are they tested?
- [ ] Any security concerns? Unvalidated inputs, credentials floating around, that kind of thing
- [ ] Would you understand the variable names in six months without context? (If not, they need renaming)
- [ ] Is there logic that gets repeated somewhere that should probably live in one place?
- [ ] Could this be slow under real traffic, not just test conditions?
- [ ] How does the code behave when things go wrong — does it handle failure, or does it just hope it doesn't happen?

**As the author:**
- [ ] Is this PR small enough that someone can genuinely review it in half an hour? If not, split it.
- [ ] Does the description explain *why* this change exists, not just what it does?
- [ ] Have you run the tests yourself before asking for a review?
- [ ] Is there leftover debug code, commented-out blocks, or orphaned TODOs?
- [ ] Would someone unfamiliar with your reasoning understand this PR without asking you anything?

---

## The part people underestimate: how you phrase things

A review can be completely correct and still cause damage. The person on the receiving end reads every comment through the lens of "is this person criticising my work or criticising me?" — and it's surprisingly easy to write comments that land badly even when you meant them fine.

Some patterns worth being aware of:

**On variable names:** there's a big difference between writing `this variable name makes no sense` and `could we rename d to deploymentDate here? — would make it much clearer to follow six months from now`. Both say the same thing. One of them makes the author feel stupid. The other just opens a conversation about naming.

**On bugs:** `this is wrong` tells the author nothing useful. What's wrong? Where? What would break? A comment like `if user is null at this point we'd get an unhandled exception — could we add a null check before line 42?` is actually actionable. That's the goal.

**On things that are fine:** most reviewers only comment when something is wrong, which means the author only ever hears about their mistakes. If something is done well — a clever approach, a clean refactor, an edge case handled neatly — say so. It takes ten seconds and it changes the whole feel of the review.

**On style:** not every comment is a blocker, and treating them the same way is a problem. If it's a real issue — a bug, a security hole, something that would break in production — make that clear. If it's a style preference, say "nit" and leave it at that. Once people learn your comments are graded by severity, they actually read them. If everything looks the same, they stop paying attention.

---

## Team norms that are worth being explicit about

Criticise the code, not the person. "This function is hard to follow" is feedback. "You write confusing code" is something else. That distinction matters more than most people realise, especially in a written medium where tone is hard to read.

Try asking rather than instructing. "What do you think about moving this logic into a helper?" and "move this into a helper" will often produce the same result, but one of them feels collaborative and the other feels like being told off. Default to the question.

Don't rubber-stamp. An Approve without any engagement is not a review — it's worse, because it gives the impression that someone checked when they didn't. If you don't have bandwidth to review properly, say so and let someone else take it. That's more honest and more useful.

On timing: try to respond within a day. Two developers waiting 48 hours for a review while they're blocked on the next task is a real cost — it compounds across the team. If you're swamped, a quick "on it tomorrow" comment goes a long way.

---