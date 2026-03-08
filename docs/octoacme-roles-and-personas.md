# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

### Interactions with Other Roles
- **Product Manager**: Clarify acceptance criteria and feature scope
- **Project Manager**: Provide effort estimates and flag technical blockers
- **QA Automation Engineer**: Hand off completed features for test coverage; pair on edge-case identification
- **UX Designer**: Review wireframes and provide implementation feasibility feedback
- **DevOps / Platform Engineer**: Collaborate on CI/CD integration and environment configuration
- **Business Analyst**: Clarify functional requirements before implementation begins

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

### Interactions with Other Roles
- **Project Manager**: Align on timeline, scope, and resource trade-offs
- **Business Analyst**: Co-own requirements gathering; review and sign off on documented requirements
- **UX Designer**: Validate designs against product goals and user research
- **Stakeholder Groups**: Gather input on business priorities; present roadmap updates
- **Developers**: Communicate acceptance criteria and answer scope questions

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

### Interactions with Other Roles
- **Product Manager**: Negotiate scope/timeline trade-offs; align on milestone readiness
- **Release Manager**: Coordinate release scheduling; escalate when release criteria are at risk
- **DevOps / Platform Engineer**: Confirm environment readiness for upcoming releases
- **Stakeholder Groups**: Provide regular status updates; surface blockers requiring stakeholder input
- **Business Analyst**: Receive requirements status updates; escalate ambiguity risks

---

## Business Analyst

### Role Summary
Business Analysts translate business objectives and stakeholder needs into clear, actionable requirements. They bridge the gap between what stakeholders want and what the delivery team builds.

### Responsibilities
- Elicit, document, and validate functional and non-functional requirements
- Facilitate requirements workshops with stakeholders and product teams
- Produce process flow diagrams, user stories, and acceptance criteria
- Support testing and validation to ensure solutions meet business needs
- Maintain a requirements traceability matrix linking business needs to delivered features

### Goals
- Ensure solutions fully address the underlying business problem
- Reduce requirements-related rework and ambiguity during development
- Support smooth handoffs between discovery and delivery

### Typical Communication
- Requirements workshops and stakeholder interviews
- User story creation in the project backlog
- Sign-off sessions with stakeholders and Product Manager

### Interactions with Other Roles
- **Product Manager**: Co-own requirements prioritization; align on scope decisions
- **Project Manager**: Report requirements status; flag scope-change risks
- **Developers**: Answer clarification questions during development; review implementations against requirements
- **UX Designer**: Collaborate on user flows to ensure requirements are reflected in designs
- **Stakeholder Groups**: Primary contact for gathering and validating business requirements
- **QA Automation Engineer**: Provide acceptance criteria that inform automated test cases

---

## UX Designer

### Role Summary
UX Designers create user flows, wireframes, and prototypes that make OctoAcme products usable, accessible, and delightful. They advocate for the end user throughout the project lifecycle.

### Responsibilities
- Conduct user research, usability testing, and competitive analysis
- Design wireframes, prototypes, and high-fidelity mockups
- Define and maintain a consistent design system and style guide
- Ensure accessibility standards (WCAG) are met
- Collaborate with Developers to achieve pixel-accurate, interaction-correct implementations

### Goals
- Ensure the product experience meets user expectations and accessibility standards
- Reduce usability issues discovered late in delivery
- Maintain design consistency across features and releases

### Typical Communication
- Design reviews in sprint planning and kickoff sessions
- Figma/prototyping tool annotations and handoff notes
- Usability testing reports shared with Product Manager and Developers

### Interactions with Other Roles
- **Product Manager**: Validate design decisions against product goals; align on user research findings
- **Business Analyst**: Map business requirements to user flows and task models
- **Developers**: Provide design specs; review implementations for fidelity and accessibility
- **QA Automation Engineer**: Share interaction specifications to support UI test automation
- **Stakeholder Groups**: Present prototypes and gather usability feedback

---

## Release Manager

### Role Summary
Release Managers coordinate end-to-end release activities across teams. They own the release plan and calendar, ensure all readiness criteria are met, and serve as the primary communication point for release-related stakeholder updates.

### Responsibilities
- Own and maintain the release calendar and release plan
- Confirm that all pre-release criteria (code freeze, CI green, security scans, release notes) are met before each release
- Coordinate go/no-go decisions with PM, Product Manager, QA, and DevOps
- Manage release communications to stakeholders and support teams
- Lead post-release verification and handoff to operations
- Drive incident escalation and rollback decisions during a release window

### Goals
- Release on schedule with minimal risk and customer impact
- Ensure every release has a documented rollback plan
- Provide clear, timely communication to all stakeholders throughout the release lifecycle

### Typical Communication
- Pre-release go/no-go meetings with PM, DevOps, and QA leads
- Release announcements and post-deploy summaries to stakeholders
- Incident bridges and status updates when release issues arise

### Interactions with Other Roles
- **Project Manager**: Align release windows with overall project timeline and dependencies
- **DevOps / Platform Engineer**: Confirm pipeline readiness, deployment steps, and environment health
- **QA Automation Engineer**: Validate that all automated and smoke tests pass before release sign-off
- **Product Manager**: Obtain product sign-off on feature completeness and scope
- **Stakeholder Groups**: Communicate release dates, scope, and any risk or delay

---

## QA Automation Engineer

### Role Summary
QA Automation Engineers design, build, and maintain automated test suites that validate product quality at speed. They integrate testing into CI/CD pipelines to catch regressions early and support continuous delivery.

### Responsibilities
- Develop and maintain automated unit, integration, and end-to-end test suites
- Integrate automated tests into CI/CD pipelines and enforce quality gates
- Analyze test results, identify flaky tests, and drive root-cause fixes
- Collaborate with Developers and Business Analysts to translate acceptance criteria into automated test cases
- Produce and share test coverage reports with the delivery team
- Support exploratory and manual testing for complex or exploratory scenarios

### Goals
- Maintain high, meaningful test coverage across critical user flows
- Reduce manual testing effort and regression risk
- Enable teams to release with confidence and speed

### Typical Communication
- Test coverage and quality reports shared at sprint reviews
- CI pipeline status updates integrated into team notifications
- Defect reports and triage sessions with Developers and PM

### Interactions with Other Roles
- **Developers**: Pair on edge-case identification; review PRs for testability; align on test data needs
- **Business Analyst**: Use acceptance criteria as the basis for automated test cases
- **Release Manager**: Confirm automated test suite passes before release go/no-go
- **DevOps / Platform Engineer**: Collaborate on CI/CD pipeline configuration and test environment stability
- **Product Manager**: Provide test coverage summaries to support release readiness decisions

---

## DevOps / Platform Engineer

### Role Summary
DevOps / Platform Engineers build and maintain the infrastructure, tooling, and pipelines that enable teams to develop, test, and ship software reliably and efficiently.

### Responsibilities
- Design, implement, and maintain CI/CD pipelines and deployment automation
- Provision and manage environments (dev, staging, production)
- Monitor system reliability, performance, and cost; respond to infrastructure incidents
- Enforce security and compliance controls in the deployment pipeline
- Enable developer productivity through improved tooling, observability, and environment stability
- Document infrastructure architecture and operational runbooks

### Goals
- Maximize system reliability, availability, and deployment frequency
- Reduce mean time to recovery (MTTR) for infrastructure incidents
- Ensure environments are consistent, secure, and auditable

### Typical Communication
- Infrastructure status and incident updates in team channels
- Deployment runbooks and environment setup guides
- Post-incident reviews and reliability reports

### Interactions with Other Roles
- **Developers**: Support local environment setup; integrate code into pipelines; advise on deployment readiness
- **Release Manager**: Coordinate deployment execution and environment readiness; participate in go/no-go decisions
- **QA Automation Engineer**: Configure test environments and CI stages for automated test execution
- **Project Manager**: Report infrastructure risks and unplanned downtime that may affect delivery timelines
- **Stakeholder Groups**: Communicate scheduled maintenance windows and infrastructure changes that affect users

---

## Stakeholder Groups

### Role Summary
Stakeholder Groups are business functions and individuals with a vested interest in project outcomes. They provide domain expertise, review deliverables, and approve milestones. Common stakeholder groups at OctoAcme include Support, Sales, Legal, Finance, and Executive Leadership.

### Responsibilities
- Provide business context, domain knowledge, and input during requirements gathering
- Review and approve key deliverables and milestone decisions
- Surface risks from their domain (e.g., legal/compliance, customer-facing impact)
- Receive and act on regular project status communications
- Escalate blockers within their functional area

### Goals
- Ensure the project delivers value to their domain and end customers
- Minimize business disruption during project delivery and releases
- Maintain visibility into project status, risks, and decisions that affect them

### Typical Communication
- Milestone reviews and stakeholder briefings (weekly or per-milestone)
- Release announcements and post-deploy summaries
- Ad-hoc escalations for high-impact decisions

### Interactions with Other Roles
- **Project Manager**: Primary point of contact for status updates and escalation
- **Product Manager**: Provide input on priorities and validate product direction
- **Business Analyst**: Participate in requirements workshops; sign off on documented requirements
- **Release Manager**: Receive release communications and confirm readiness from their domain

#### Common Stakeholder Group Examples
| Group | Typical Contribution |
|-------|----------------------|
| **Support** | Input on known customer pain points; review of support-facing release notes |
| **Sales** | Roadmap input; coordination of customer-facing announcements |
| **Legal / Compliance** | Review of privacy, security, and regulatory requirements; approval of compliance controls |
| **Finance** | Budget approvals; cost forecasting and review |
| **Executive Leadership** | Strategic direction; sponsor-level escalation and decision authority |

---

## How to Use These Personas in Process Docs

Each OctoAcme process document references roles to clarify ownership and accountability. Use the following guidelines when applying personas across lifecycle docs:

### RACI Alignment
Refer to [`octoacme-raci-ownership-matrix.md`](./octoacme-raci-ownership-matrix.md) to see which role is **R**esponsible, **A**ccountable, **C**onsulted, or **I**nformed for each major artifact and milestone.

### Phase Ownership
Each project phase has a primary owner and supporting roles. For phase-by-phase handoff responsibilities and sign-off requirements, see [`octoacme-phase-handoff-checklist.md`](./octoacme-phase-handoff-checklist.md).

### Role-Specific Guidance in Copilot Spaces
- Use each persona definition as a persona prompt for Copilot Spaces to get role-specific guidance.
- For example, loading the "Release Manager" persona focuses Copilot Spaces on release planning, go/no-go criteria, and stakeholder communication.

### Quick Ownership Reference

| Activity | Primary Owner | Key Collaborators |
|----------|---------------|-------------------|
| Requirements gathering | Business Analyst | Product Manager, Stakeholders |
| Backlog prioritization | Product Manager | Project Manager, Business Analyst |
| Sprint planning & delivery | Project Manager | Developers, QA Automation Engineer |
| UI/UX design | UX Designer | Product Manager, Developers |
| Test automation | QA Automation Engineer | Developers, DevOps |
| Release coordination | Release Manager | DevOps, QA, PM, Product Manager |
| Infrastructure & pipelines | DevOps / Platform Engineer | Developers, Release Manager |
| Stakeholder communication | Project Manager | Release Manager, Product Manager |

