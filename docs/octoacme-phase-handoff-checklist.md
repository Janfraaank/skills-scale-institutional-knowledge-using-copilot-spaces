# OctoAcme — Phase Handoff & Release Readiness Checklists

## Purpose
Ensure clean, documented transitions between project phases and a consistent gate before every release. Each checklist identifies who owns the sign-off and what must be true before work proceeds to the next phase.

> For role definitions, see [`octoacme-roles-and-personas.md`](./octoacme-roles-and-personas.md).  
> For artifact ownership, see [`octoacme-raci-ownership-matrix.md`](./octoacme-raci-ownership-matrix.md).

---

## Phase 1 → Phase 2: Initiation → Planning Handoff

**Sign-off owner:** Project Manager  
**Secondary sign-off:** Product Manager (confirms business alignment)

### Required before moving to Planning

- [ ] Project One-pager is complete and reviewed by the Product Manager
- [ ] Problem statement and success metrics are clearly defined and agreed upon
- [ ] Stakeholder list is documented with communication preferences
- [ ] Initial risk list created and reviewed with the team
- [ ] High-level timeline and key milestones drafted
- [ ] Proposed team / roles identified (see [`octoacme-roles-and-personas.md`](./octoacme-roles-and-personas.md))
- [ ] RACI matrix drafted (see [`octoacme-raci-ownership-matrix.md`](./octoacme-raci-ownership-matrix.md))
- [ ] Sponsor / Stakeholder alignment confirmed (meeting notes or email approval on file)
- [ ] Go / No-go decision: **Approved to proceed to Planning**

**Signed off by (PM):** _________________________ **Date:** _____________  
**Signed off by (Product Manager):** _____________ **Date:** _____________

---

## Phase 2 → Phase 3: Planning → Execution Handoff

**Sign-off owner:** Project Manager  
**Secondary sign-off:** Product Manager (backlog readiness), QA Automation Engineer (test plan readiness)

### Required before moving to Execution

- [ ] Project kickoff meeting held; notes distributed to team and stakeholders
- [ ] Prioritized backlog created with acceptance criteria on all Sprint 1 items
- [ ] Scope, milestones, and release plan agreed upon by PM, Product Manager, and Release Manager
- [ ] Definition of Done documented and agreed by the delivery team
- [ ] RACI matrix finalized and distributed to all stakeholders
- [ ] Risk register populated; top risks have assigned owners and mitigation plans
- [ ] Initial test plan or QA approach drafted by QA Automation Engineer
- [ ] Development environment and CI pipeline verified by DevOps / Platform Engineer
- [ ] Design assets (wireframes/prototypes) available for Sprint 1 features (UX Designer sign-off)
- [ ] Business Analyst has documented requirements for all Sprint 1 backlog items
- [ ] Team capacity confirmed and sprint calendar set

**Signed off by (PM):** _________________________ **Date:** _____________  
**Signed off by (Product Manager):** _____________ **Date:** _____________  
**Signed off by (QA Automation Engineer):** _______ **Date:** _____________

---

## Phase 3 → Phase 4: Execution → Release Handoff

**Sign-off owner:** Release Manager  
**Secondary sign-off:** Project Manager, QA Automation Engineer, DevOps / Platform Engineer

### Required before handing off to the Release phase

- [ ] All acceptance criteria for the release scope have been met and verified
- [ ] All PRs for the release are merged; no open PRs in the release scope
- [ ] CI pipeline is green (tests, lint, security scans all passing)
- [ ] QA Automation Engineer confirms automated test suite coverage is sufficient
- [ ] Manual / exploratory testing completed for high-risk areas
- [ ] Release notes drafted and reviewed by Release Manager and Product Manager
- [ ] Rollback / mitigation plan documented by Release Manager and DevOps
- [ ] Staging environment deployment successful with smoke tests passing
- [ ] DevOps / Platform Engineer confirms production environment is healthy and ready
- [ ] Release Manager has confirmed go/no-go with PM, Product Manager, QA, and DevOps
- [ ] Stakeholder communication for the upcoming release drafted and ready to send

**Signed off by (Release Manager):** ______________ **Date:** _____________  
**Signed off by (PM):** __________________________ **Date:** _____________  
**Signed off by (QA Automation Engineer):** _______ **Date:** _____________  
**Signed off by (DevOps / Platform Engineer):** ____ **Date:** _____________

---

## Phase 4 → Phase 5: Release → Retrospective Handoff

**Sign-off owner:** Project Manager  
**Secondary sign-off:** Release Manager (confirms post-deploy stable)

### Required before closing the release and moving to Retrospective

- [ ] Production deployment completed successfully
- [ ] Post-deploy verification completed by QA Automation Engineer and DevOps
- [ ] Release announcement sent to stakeholders and support teams by Release Manager
- [ ] No critical production incidents outstanding from this release
- [ ] Monitoring dashboards reviewed; no anomalies requiring immediate action
- [ ] Release notes published to the appropriate channel / documentation site
- [ ] Any open incidents from the release have assigned owners and timelines

**Signed off by (Release Manager):** ______________ **Date:** _____________  
**Signed off by (PM):** __________________________ **Date:** _____________

---

## Release Readiness Checklist (Detailed)

Use this checklist for every release type (Patch, Minor, Major). Ownership is noted for each item.

> Reference: [`octoacme-release-and-deployment.md`](./octoacme-release-and-deployment.md)

### Code & Quality

| Item | Owner | Status |
|------|-------|--------|
| All in-scope features implemented and acceptance criteria verified | Developers | ☐ |
| All PRs merged to the release branch | Developers | ☐ |
| Automated test suite passing in CI (unit, integration, E2E) | QA Automation Engineer | ☐ |
| No known Critical or High severity defects open in release scope | QA Automation Engineer | ☐ |
| Security scan passing (SAST, dependency vulnerabilities) | DevOps / Platform Engineer | ☐ |
| Code coverage meets or exceeds team-defined threshold | QA Automation Engineer | ☐ |
| Technical debt items from this release logged for backlog | Developers | ☐ |

### Documentation & Communication

| Item | Owner | Status |
|------|-------|--------|
| Release notes drafted and approved | Release Manager | ☐ |
| API / integration documentation updated (if applicable) | Developers / Business Analyst | ☐ |
| Support team briefed on new features and known issues | Release Manager | ☐ |
| Stakeholder release communication prepared | Release Manager | ☐ |
| Deployment runbook updated (if steps changed) | DevOps / Platform Engineer | ☐ |

### Infrastructure & Environments

| Item | Owner | Status |
|------|-------|--------|
| Staging deployment completed and smoke tests passed | DevOps / Platform Engineer | ☐ |
| Production environment health verified (capacity, configuration) | DevOps / Platform Engineer | ☐ |
| Database migrations tested in staging (if applicable) | DevOps / Platform Engineer + Developers | ☐ |
| Rollback / restore procedure documented and tested | DevOps / Platform Engineer | ☐ |
| Deployment window scheduled and communicated | Release Manager | ☐ |
| On-call rotation confirmed for deployment window | DevOps / Platform Engineer | ☐ |
| Feature flags configured correctly for the release | Developers + DevOps | ☐ |

### Go / No-Go Decision

| Approver | Approval Required | Sign-off |
|----------|------------------|---------|
| Release Manager | Yes — accountable for release | ☐ Approved / ☐ Blocked |
| Project Manager | Yes — confirms scope and timeline | ☐ Approved / ☐ Blocked |
| Product Manager | Yes — confirms feature completeness | ☐ Approved / ☐ Blocked |
| QA Automation Engineer | Yes — confirms quality gate | ☐ Approved / ☐ Blocked |
| DevOps / Platform Engineer | Yes — confirms infrastructure readiness | ☐ Approved / ☐ Blocked |

> **Release proceeds only when all approvers have marked Approved.** Any "Blocked" status must be resolved or formally risk-accepted by the Release Manager and Project Manager before proceeding.

---

## Retrospective Handoff Checklist

**Sign-off owner:** Project Manager

### Required before closing the project / iteration

- [ ] Retrospective meeting held with full delivery team
- [ ] Retrospective notes and key themes documented and shared
- [ ] Action items captured with owners and due dates
- [ ] Action items added to the team backlog or tracked in the project board
- [ ] Process improvement proposals submitted to PM for prioritization
- [ ] Lessons learned archived in the project repo or knowledge base
- [ ] Final project status report sent to stakeholders

**Signed off by (PM):** _________________________ **Date:** _____________
