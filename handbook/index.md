# 📘 Engineering Handbook — Best Practices

> **Maintenu par :** Antonin Miranda · Kylian Tranchet · Hugo Denis  
> **Dernière mise à jour :** April 2026  
> **Repo :** Public GitHub — contributions via Pull Request uniquement

---

## Purpose

This handbook exists because we had a problem: 20 engineers, 20 different ways of doing things, and too many bugs reaching production.

Rather than enforce rules top-down, we chose to write down what actually works — based on real experience, real articles, and real mistakes. This document is a living reference. It is not a rulebook to follow blindly; it is a shared baseline to build on.

**Who this is for:**
- New engineers joining the team — read this before your first sprint
- Existing engineers — use it to align on expectations and resolve disagreements
- Anyone opening a PR, running an estimation session, or pushing to main

---

## How to Use This Handbook

This handbook is designed to be **skimmed, not read cover to cover.** Each section is self-contained. Jump to whatever is relevant to what you are working on right now.

Each section covers:
- A brief introduction to the topic and why it matters
- ✅ Good practices to follow
- ❌ Bad practices to avoid
- At least one diagram to make things concrete
- Links to the best external resources for deeper reading

If you disagree with something here, open a PR and make your case. This document improves through discussion.

---

## Table of Contents

| # | Topic | Description |
|---|---|---|
| 1 | [Introduction](./index.md) | Purpose and structure of this handbook |
| 2 | [Task Estimation in Scrum](./task-estimation.md) | How to estimate work reliably, run Planning Poker, and avoid common traps |
| 3 | [Code Reviews](./code-reviews.md) | How to give and receive useful feedback, keep PRs small, and avoid bottlenecks |
| 4 | [CI/CD](./ci-cd.md) | How to build reliable pipelines, automate testing, and deploy with confidence |
---

## Individual Contributions

| Team Member | Contributions | Verified by |
|---|---|---|
| **Antonin Miranda** | - Set up the repository and branch protection rules<br>- Wrote the Project Plan and assigned tasks<br>- Led the Task Estimation section (research + writing)<br>- Contributed to the CI/CD section<br>- Wrote the Retrospective | Kylian, Hugo |
| **Kylian Tranchet** | - Defined the handbook structure and created this index<br>- Wrote the Task Estimation section (co-author)<br>- Led the Code Reviews section (research + writing)<br>- Standardised formatting across all files<br>- Reviewed all PRs and gave written feedback | Antonin, Hugo |
| **Hugo Denis** | - Led the CI/CD section (research + writing)<br>- Co-authored the Code Reviews section<br>- Created all Mermaid diagrams for CI/CD and Code Reviews<br>- Compiled the Individual Contributions table<br>- Participated in all PR reviews | Antonin, Kylian |

---

## Contributing to This Handbook

Follow the same process as any code change:

1. Create a branch from `main` (`docs/your-topic`)
2. Make your changes
3. Open a Pull Request with a clear description
4. Get 2 approvals before merging
5. Never merge your own PR without review

See the [Project Plan](../PROJECT_PLAN.md) for full workflow details.