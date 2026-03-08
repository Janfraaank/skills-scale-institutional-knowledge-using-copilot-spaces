# OctoAcme — RACI & Ownership Matrix Template

## Purpose
Define who is **R**esponsible, **A**ccountable, **C**onsulted, and **I**nformed for each key artifact and milestone in an OctoAcme project. Fill in this template at the start of planning and update it when team composition or scope changes.

> For role definitions, see [`octoacme-roles-and-personas.md`](./octoacme-roles-and-personas.md).

## RACI Key

| Code | Meaning |
|------|---------|
| **R** | **Responsible** — Does the work; owns the task day-to-day |
| **A** | **Accountable** — Ultimate decision-maker; signs off on completion |
| **C** | **Consulted** — Provides input before or during the work |
| **I** | **Informed** — Notified of progress or completion; no action required |

> Each artifact/milestone should have **exactly one A** (Accountable). There may be multiple Rs, Cs, and Is.

---

## Project RACI Matrix

**Project name:**
**Version / Date:**
**Owner (PM):**

Replace `[Name/Team]` with actual names or team identifiers for your project.

### Initiation Phase

| Artifact / Milestone | Project Manager | Product Manager | Business Analyst | Developers | UX Designer | Release Manager | QA Automation Engineer | DevOps / Platform Eng. | Stakeholder Groups |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Project One-pager | **A** | C | C | I | I | I | I | I | C |
| Stakeholder list & comms plan | **A** | C | R | I | I | I | I | I | C |
| Initial risk list | **A** | C | C | C | I | I | I | C | I |
| Go / No-go decision | C | **A** | C | I | I | I | I | I | C |

### Planning Phase

| Artifact / Milestone | Project Manager | Product Manager | Business Analyst | Developers | UX Designer | Release Manager | QA Automation Engineer | DevOps / Platform Eng. | Stakeholder Groups |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Prioritized backlog | C | **A** | R | C | C | I | I | I | C |
| Acceptance criteria | C | **A** | R | C | C | I | C | I | I |
| Definition of Done | **A** | C | C | R | I | C | C | C | I |
| Release plan & milestones | **A** | C | I | C | I | R | I | C | I |
| Initial test plan | C | I | C | C | I | I | **A** | C | I |
| Risk register | **A** | C | C | C | I | C | I | C | I |
| RACI matrix (this doc) | **A** | C | C | I | I | I | I | I | I |

### Execution & Tracking Phase

| Artifact / Milestone | Project Manager | Product Manager | Business Analyst | Developers | UX Designer | Release Manager | QA Automation Engineer | DevOps / Platform Eng. | Stakeholder Groups |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Sprint plan | **A** | C | I | R | I | I | C | I | I |
| Feature implementation | C | I | C | **A** | C | I | C | C | I |
| UI / UX designs | I | C | C | C | **A** | I | I | I | C |
| Automated test suite | I | I | C | C | I | I | **A** | C | I |
| CI/CD pipeline | I | I | I | C | I | I | C | **A** | I |
| Weekly status report | **A** | C | I | I | I | C | I | I | I |
| Blocker escalation | **A** | C | I | R | I | C | I | C | I |

### Release Phase

| Artifact / Milestone | Project Manager | Product Manager | Business Analyst | Developers | UX Designer | Release Manager | QA Automation Engineer | DevOps / Platform Eng. | Stakeholder Groups |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Release readiness go/no-go | C | C | I | I | I | **A** | C | C | C |
| Release notes | C | C | I | R | I | **A** | I | I | I |
| Staging deployment | I | I | I | C | I | C | C | **A** | I |
| Production deployment | I | I | I | I | I | **A** | C | R | I |
| Post-deploy verification | I | I | I | C | I | **A** | R | C | I |
| Stakeholder release comms | C | C | I | I | I | **A** | I | I | I |
| Rollback decision | C | C | I | C | I | **A** | C | R | I |

### Retrospective Phase

| Artifact / Milestone | Project Manager | Product Manager | Business Analyst | Developers | UX Designer | Release Manager | QA Automation Engineer | DevOps / Platform Eng. | Stakeholder Groups |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Retrospective facilitation | **A** | C | I | R | I | C | C | C | I |
| Action item tracking | **A** | C | I | R | I | R | R | R | I |
| Process improvement proposals | **A** | C | C | C | C | C | C | C | I |

---

## How to Customize This Template

1. **Copy this file** and rename it for your project (e.g., `raci-project-foo-2026.md`).
2. **Fill in project details** (name, version, PM owner) at the top.
3. **Replace or add rows** for any additional artifacts specific to your project.
4. **Verify each row has exactly one A** before finalizing.
5. **Review with the team** at kickoff and update when roles or scope change.
6. **Link this matrix** from your project One-pager and planning docs for easy reference.

---

## Escalation Ownership Quick Reference

| Situation | First Owner | Escalates To |
|-----------|-------------|-------------|
| Blocked feature / task | Developer | Project Manager |
| Scope change request | Business Analyst / Product Manager | Project Manager → Sponsor |
| Release risk or delay | Release Manager | Project Manager → Sponsor |
| Infrastructure incident | DevOps / Platform Engineer | Release Manager → Project Manager |
| Security / compliance concern | DevOps / Platform Engineer | Project Manager → Legal / Security |
| Stakeholder conflict | Project Manager | Product Manager → Sponsor |
