# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

> **Related docs:**
> - Role definitions (Release Manager, DevOps, QA Automation Engineer): [`octoacme-roles-and-personas.md`](./octoacme-roles-and-personas.md)
> - Release readiness checklist & go/no-go sign-offs: [`octoacme-phase-handoff-checklist.md`](./octoacme-phase-handoff-checklist.md#release-readiness-checklist-detailed)
> - RACI for release phase: [`octoacme-raci-ownership-matrix.md`](./octoacme-raci-ownership-matrix.md#release-phase)

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Release Ownership

| Responsibility | Owner | Collaborators |
|---------------|-------|---------------|
| Release plan & calendar | **Release Manager** | Project Manager |
| Go / No-go decision | **Release Manager** | Project Manager, Product Manager, QA Automation Engineer, DevOps |
| Pipeline & deployment execution | **DevOps / Platform Engineer** | Release Manager |
| Automated test sign-off | **QA Automation Engineer** | Release Manager |
| Release notes & stakeholder comms | **Release Manager** | Product Manager, Project Manager |
| Rollback decision | **Release Manager** | DevOps / Platform Engineer |

> For detailed role descriptions, see [`octoacme-roles-and-personas.md`](./octoacme-roles-and-personas.md).

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared

## Deployment Checklist
- [ ] **Release Manager**: Deployment window scheduled and communicated
- [ ] **DevOps / Platform Engineer**: Backup or snapshot taken (if applicable)
- [ ] **DevOps / Platform Engineer**: Deploy to staging and run smoke tests
- [ ] **QA Automation Engineer**: Automated test suite passing in staging
- [ ] **DevOps / Platform Engineer**: Deploy to production (automated pipeline preferred)
- [ ] **QA Automation Engineer + DevOps**: Run post-deploy verifications
- [ ] **Release Manager**: Announce release to stakeholders and support

> For the full release readiness gate (code quality, documentation, infrastructure, go/no-go approvals), see [`octoacme-phase-handoff-checklist.md`](./octoacme-phase-handoff-checklist.md#release-readiness-checklist-detailed).

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
