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
