# Project Plan

> **Team:** Antonin Miranda A00048051 · Kylian Tranchet A00048049 · Hugo Denis A00048052
> **Deadline:** April 5, 2026 — 10:00 PM
> **Repository:** Public GitHub (Markdown)
> **Process:** Trunk-based Development (short-lived branches + Pull Requests)

---

## Chosen Topics

1. Task Estimation in Scrum
2. Code Reviews
3. CI/CD (Continuous Integration and Deployment)

**Why CI/CD?** It directly addresses the problems described in the brief, bugs reaching production and unpredictable progress. There is also a wealth of practical, experience-based resources on the subject, which aligns with the handbook's focus on real-world guidance over theory.

---

## Repository Structure

```
.
├── README.md
├── PROJECT_PLAN.md
├── RETROSPECTIVE.md
├── handbook/
│   ├── index.md               ← introduction and table of contents
│   ├── task-estimation.md
│   ├── code-reviews.md
│   └── ci-cd.md
└── assets/
    └── images/
```

---

## Task Breakdown & Responsibilities

| Task | Owner | Contributor | Branch |
|---|---|---|---|
| Repository setup + project plan | Antonin | — | `docs/project-plan` |
| Handbook introduction & structure | Kylian | — | `docs/handbook-intro` |
| Task Estimation section | Antonin | Kylian | `feat/task-estimation` |
| Code Reviews section | Kylian | Hugo | `feat/code-reviews` |
| CI/CD section | Hugo | Antonin | `feat/ci-cd` |
| Individual contributions table | Hugo | — | `docs/contributions-table` |
| Retrospective | Antonin | Kylian, Hugo | `docs/retrospective` |
| Final review & formatting | Kylian | — | `fix/formatting-consistency` |

> Each topic must have at least **2 contributors** in the commit history. Everyone must also participate in reviewing Pull Requests.

---

## Git Workflow

We follow **Trunk-based Development**:

- `main` is the protected branch — no direct commits (except the initial repo setup)
- Each task lives on its own short-lived branch
- Work is merged into `main` via Pull Request
- Every PR requires **2 approvals** before merging
- Reviews must include constructive feedback, not just approvals

```
main
 ├── docs/project-plan
 ├── docs/handbook-intro
 ├── feat/task-estimation
 ├── feat/code-reviews
 ├── feat/ci-cd
 ├── docs/contributions-table
 ├── docs/retrospective
 └── fix/formatting-consistency
```

---

## Timeline

The three handbook topics (Phases 3a, 3b, 3c) can be worked on in parallel since they are on separate branches.

| Phase | Tasks | Who |
|---|---|---|
| **1 — Repo setup** | Create repo, add .gitignore, README, project plan | Antonin |
| **2 — Handbook structure** | Create intro, placeholder files, assets folder | Kylian |
| **3 — Content (parallel)** | Write all three topic sections | All |
| **4 — Finalisation** | Contributions table, retrospective, formatting pass | Hugo, Antonin, Kylian |

---

## Handbook Content Guidelines

Each section should:
- Be between **500 and 1000 words**
- Include at least **5 quality sources** (prioritising practitioner experience over theory)
- Cover both **good practices** and **bad practices to avoid**
- Include at least **1 diagram or visual**
- Link to all reference articles

---

## Final Checklist

- [ ] Repository is public on GitHub
- [ ] `PROJECT_PLAN.md` is complete
- [ ] `RETROSPECTIVE.md` is complete
- [ ] Each topic has 5 quality sources with links
- [ ] Each topic is 500–1000 words
- [ ] Each topic has at least 1 diagram
- [ ] Each topic has at least 2 contributors in the commit history
- [ ] Each PR was reviewed by 2 members with meaningful comments
- [ ] Contributions table is complete and cross-verified
- [ ] All Markdown links work correctly on GitHub
- [ ] Repository link submitted on Brightspace before deadline
