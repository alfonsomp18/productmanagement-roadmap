# GitHub Setup Guide

This document helps configure labels, milestones, and a project board.

## 1) Create Labels

Option A: Create manually in GitHub settings using `docs/labels.json`.

Option B: Use GitHub CLI (`gh`) and `jq`:

```bash
jq -c '.[]' docs/labels.json | while read -r label; do
  gh label create "$(echo "$label" | jq -r '.name')" \
    --color "$(echo "$label" | jq -r '.color')" \
    --description "$(echo "$label" | jq -r '.description')" \
    --force
 done
```

## 2) Create Milestones

Create these milestones:

- Q2-2026
- Q3-2026
- Q4-2026

Using `gh`:

```bash
gh api repos/{owner}/{repo}/milestones -f title='Q2-2026'
gh api repos/{owner}/{repo}/milestones -f title='Q3-2026'
gh api repos/{owner}/{repo}/milestones -f title='Q4-2026'
```

## 3) Create GitHub Project Board (Kanban)

Create a project named `Product Roadmap` with columns:

- Backlog
- Planned
- In Progress
- Review
- Done

Then:

1. Add roadmap issues to the project.
2. Use `status:*` labels in parallel with project columns.
3. Review board weekly and roadmap docs monthly.

## 4) Seed Example Issues

Create 4 issues from `features/example-features.md`:

- #101 Onboarding checklist with progress tracker
- #102 Welcome email journey with contextual nudges
- #103 API key self-service management
- #104 Webhook delivery reliability dashboard

Assign milestones and labels based on the examples.
