# Product Roadmap System (GitHub-Native)

This repository is a centralized, GitHub-based product roadmap designed for both technical and non-technical stakeholders.

It creates a clear chain from strategy to execution:

**Vision → Initiative → Feature → Issue → Delivery**

---

## Product Overview

This system helps product teams:

- Define and communicate strategic priorities
- Plan by quarter using simple roadmap views
- Track execution with GitHub Issues, labels, milestones, and a project board
- Keep roadmap context close to day-to-day delivery work

---

## Repository Structure

```text
/roadmap/
  README.md
  now.md
  next.md
  later.md
  backlog.md

/initiatives/
  initiative-template.md
  onboarding-activation-improvement.md
  api-partner-expansion.md

/features/
  feature-template.md
  example-features.md

/docs/
  product-vision.md
  principles.md
  labels.json
  github-setup.md

.github/
  ISSUE_TEMPLATE/
    feature_request.md
    bug_report.md
```

---

## How the Roadmap Works

### 1) Strategic Themes (`/docs/product-vision.md`)
High-level, long-horizon direction.

Example: "Improve user onboarding".

### 2) Initiatives (`/initiatives/*.md`)
Mid-level outcomes that explain what we are trying to improve and how success is measured.

### 3) Features (GitHub Issues)
Execution-level work items linked to initiatives and milestones.

---

## Planning Cadence (Now / Next / Later)

- `roadmap/now.md` → In progress now
- `roadmap/next.md` → Planned next quarter
- `roadmap/later.md` → Longer-term ideas
- `roadmap/backlog.md` → Unprioritized options

Each roadmap item includes:

- Status emoji (`🟢` in progress, `🟡` planned, `⚪` idea)
- Link to an initiative file and/or issue
- Owner and milestone where relevant

---

## How to Contribute

1. Read the vision in `docs/product-vision.md`.
2. Check roadmap files under `roadmap/`.
3. If work exists, comment on the linked issue.
4. If work is new, create a feature request issue from the template.
5. Link the issue to an initiative and milestone.
6. Add/update the issue in the GitHub project board.

---

## How to Create Features

Use `.github/ISSUE_TEMPLATE/feature_request.md` and include:

- Problem statement
- Proposed solution
- Acceptance criteria
- Linked initiative

Then apply labels:

- One `type:*`
- One `priority:*`
- One `status:*`
- One `area:*`

Finally set a milestone (`Q2-2026`, `Q3-2026`, `Q4-2026`) and add to the project board.

---

## Linking Work to the Roadmap

Use this linking model:

1. Vision theme referenced in initiative
2. Initiative linked in feature issue body
3. Issue referenced in `roadmap/now.md`, `next.md`, `later.md`, or `backlog.md`

This provides full traceability from strategy to execution.

---

## GitHub Setup (Labels, Milestones, Project Board)

Setup instructions and optional `gh` CLI commands are in:

- `docs/labels.json`
- `docs/github-setup.md`

