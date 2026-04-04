# Task Estimation in Scrum

## Introduction

Nobody gets estimation right. That's not pessimism, it's just the track record. The idea sounds reasonable enough: figure out how long things take, plan your sprints accordingly, tell stakeholders what to expect. In practice the estimates are usually wrong, sometimes badly, and the reasons vary. The team was optimistic. Someone pushed back before the conversation even started. The task looked straightforward until you opened it up and found three other problems hiding inside.

The framing matters more than people admit. In Scrum, an estimate isn't a commitment, it's a guess used to have a better conversation about what to build and when. Teams that lose sight of that end up in a specific kind of dysfunction, developers padding their numbers to avoid blame, managers treating a missed estimate like a broken contract. Getting the framing right doesn't fix everything, but getting it wrong poisons everything else.

This chapter goes into what the research and practitioner experience actually say with a genuine disagreement about whether estimation is worth doing at all.

---

## Sources and Perspectives

These sources were picked because the people behind them had real problems, not theoretical ones. They changed how they worked based on what they saw.

### 1. Ron Jeffries — *Story Points Revisited* (2019)

Jeffries co-created Extreme Programming and is generally credited with inventing story points. Which makes it notable that he wrote a piece essentially apologizing for them. Across team after team, he watched the same thing happen, points stopped being a tool for the team and became a metric for managers. Velocity tracked on dashboards, developers gaming scores to look productive. His line, *"I may have invented story points, and if I did, I'm sorry"*, is blunt, and he means it. The idea wasn't bad. What people did with it was.
🔗 https://ronjeffries.com/articles/019-01ff/story-points/Index.html

### 2. Tim Ottinger — *Stop Using Story Points* (Industrial Logic, 2019)

Ottinger watched teams estimate for years. The pattern he kept seeing, it didn't matter much how many points a task got assigned. Teams still closed roughly the same number of items per week. The points weren't predicting throughput, they were just adding a step. After tracking this across dozens of teams, his conclusion was pretty simple: *"We get about 8 things done each week, no estimation required."* Cut stories small enough that they're comparable in size, then count what ships. That's your data.
🔗 https://www.industriallogic.com/blog/stop-using-story-points/

### 3. Eiki Takeuchi — *3 Critical Reasons I Stopped Using Story Points* (Medium, 2023)

Takeuchi didn't arrive at his skepticism quickly. It built up over several projects until the problems were hard to ignore. Three things kept happening: the reference frame for what a "3" or a "5" meant drifted badly over time, developers started underestimating to look faster, and discussions in planning sessions shifted toward arguing about the number rather than understanding the problem. That last one is maybe the most damaging, a genuine conversation about complexity has value; debating whether something is a 5 or an 8 usually doesn't.
🔗 https://medium.com/beyond-agile-leadership/3-critical-reasons-i-stopped-using-story-points-ca8b596e9f56

### 4. Allen Holub — *#NoEstimates* (blog & conferences, 2012–present)

Holub's position is the most radical, the problem isn't how teams estimate, it's that they estimate at all. Time spent on estimation is time not spent building. And once an estimate exists, it tends to calcify, stakeholders anchor on it, deadlines get locked in, and the team ends up accountable to a number nobody ever intended as a commitment. His alternative is the same one Ottinger lands on from a different direction, slice work small enough that pieces are roughly equivalent, count how many ship per week, use that as your planning baseline.
🔗 https://holub.com/noestimates/

### 5. Mike Cohn — *Are We Really Bad at Estimating?* (Mountain Goat Software, 2021)

Cohn disagrees with the others, and he brings actual data. Across hundreds of projects, teams that estimated consistently got better at it over time. His argument is that the tool isn't broken, the execution is. Estimates made in five minutes, stories that never get split, velocity that nobody looks at after the sprint. When teams take estimation seriously as a practice and actually review how their predictions compare to what happened, it works. When they treat it as a box to check, of course it doesn't.
🔗 https://www.mountaingoatsoftware.com/blog/are-we-really-bad-at-estimating

---

## Where They Agree

The five perspectives above don't land in the same place. But three things come up across all of them, regardless of which side of the debate someone is on.

The first is what happens when estimation gets used for control. Jeffries, Takeuchi, and Holub all describe the same drift independently, a tool built for team planning gets turned into a way to measure individual productivity. Once developers know their estimates are being tracked, they stop estimating honestly and start managing the number. The original signal disappears.

The second is that story size is the real variable. Ottinger and Holub both conclude that if tasks are small and roughly comparable, you don't need to estimate them, you just count. Cohn, even while defending estimation, says you can't do it reliably without splitting first. Everyone agrees the stories need to be small. What they disagree on is what to do once they are.

The third is that estimates made under pressure aren't estimates, they're theater. A fixed deadline, a manager in the room, social pressure to commit to a number: any of these will push the team toward a figure that reflects the pressure, not the work. You end up with false precision. A number that looks like data and carries no actual information.

---

## The Process: Planning Poker

Planning Poker is how most Scrum teams estimate in practice. Everyone picks a card from the Fibonacci sequence (1, 2, 3, 5, 8, 13, 21, ...) in private, then reveals simultaneously. When people converge, you have an estimate. When they diverge, a junior dev cards a 13, a senior cards a 3, you have something more useful, a reason to ask why, which usually surfaces an assumption or a risk nobody had made explicit.

```
          ┌─────────────────────────────────────────┐
          │           PLANNING POKER FLOW            │
          └─────────────────────────────────────────┘

  1. Product Owner presents the user story
          │
          ▼
  2. Each member secretly picks a card
     [ 1 ]  [ 2 ]  [ 3 ]  [ 5 ]  [ 8 ]  [ 13 ]  [ 21 ]
          │
          │
     ┌────┴────┐
     │         │
  Consensus  Divergence
     │         │
     ▼         ▼
  Estimate   Discussion → New estimate
  accepted   (extremes explain their vote)
```

The Fibonacci sequence matters here. The gaps widen as the numbers go up, which is a built-in acknowledgment that uncertainty scales with complexity. A task that might be a 13 could easily be a 21, and the scale forces the team to sit with that rather than pretend otherwise.

---

## What Works

Relative estimation beats absolute estimation. Saying "this is roughly twice as involved as the last one" is more reliable than guessing hours, because humans are genuinely better at comparison than prediction. Use that.

Get everyone in the room. A junior dev and a senior dev often see the same task very differently, and that gap is worth knowing about. If one person estimates for the group, you lose the disagreements, which is where most of the useful information lives.

Anything that comes in above 13 points needs to be split before it touches a sprint. A story that big almost always has complexity hiding inside it, or decisions that haven't been made yet. Find those before the sprint starts, not during.

After a few sprints, use actual velocity — not theoretical capacity. Planning based on "everyone's fully available and nothing will break" is not planning. Use the numbers from the last few sprints and adjust from there.

When something turns out harder than expected mid-sprint, say so. Forcing a rushed delivery to honor an estimate that was wrong helps nobody. The estimate was a guess; the working software is what matters.

---

## What Breaks It

The estimate is already decided before the discussion starts. If a manager has floated a number, or a deadline implies one, the team's estimate will drift toward it. That's not estimation, it's anchoring. The result is a number that reflects what someone wanted to hear, not what the team actually thinks.

Converting points to hours. Points are a relative measure of complexity, not a unit of time. The moment you convert them, you're making a promise you didn't intend to make, and giving developers a debt to repay rather than a problem to solve.

Planning against ideal conditions. Full team, no interruptions, no production fires, this is not the sprint you're going to have. Use actual velocity from the last few sprints. Consistently optimistic capacity planning leads to consistently overcommitted sprints, and the team stops trusting the process.

One person estimating. Solo estimation means one person's blind spots become everyone's blind spots. On anything with hidden dependencies, this is where things go wrong.

Penalizing missed estimates. If developers believe a missed estimate will be held against them, they pad everything. The estimates stop meaning anything, and the data you're using to plan becomes noise. An estimate is a guess about uncertain work — treating it as a performance target is the fastest way to break the whole system.

---

## References

1. Ron Jeffries — *Story Points Revisited*: https://ronjeffries.com/articles/019-01ff/story-points/Index.html
2. Tim Ottinger — *Stop Using Story Points*: https://www.industriallogic.com/blog/stop-using-story-points/
3. Eiki Takeuchi — *3 Critical Reasons I Stopped Using Story Points*: https://medium.com/beyond-agile-leadership/3-critical-reasons-i-stopped-using-story-points-ca8b596e9f56
4. Allen Holub — *#NoEstimates*: https://holub.com/noestimates/
5. Mike Cohn — *Are We Really Bad at Estimating?*: https://www.mountaingoatsoftware.com/blog/are-we-really-bad-at-estimating
