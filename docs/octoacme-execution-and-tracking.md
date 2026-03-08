# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

> **Related docs:**
> - Role definitions: [`octoacme-roles-and-personas.md`](./octoacme-roles-and-personas.md)
> - RACI / Ownership matrix: [`octoacme-raci-ownership-matrix.md`](./octoacme-raci-ownership-matrix.md)
> - Execution → Release handoff checklist: [`octoacme-phase-handoff-checklist.md`](./octoacme-phase-handoff-checklist.md)

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup — **Developer** surfaces blocker; **Project Manager** facilitates resolution
- Level 2: **Project Manager** escalates to **Product Manager** and dependent teams; **Release Manager** or **DevOps / Platform Engineer** engaged when the blocker affects a release window or production environment
- Level 3: Sponsor-level escalation for business-impacting issues — **Project Manager** owns communication to sponsor/stakeholders

> For a full escalation ownership reference, see [`octoacme-raci-ownership-matrix.md`](./octoacme-raci-ownership-matrix.md#escalation-ownership-quick-reference).

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
- [ ] Phase handoff checklist completed before handing off to Release: [`octoacme-phase-handoff-checklist.md`](./octoacme-phase-handoff-checklist.md)
