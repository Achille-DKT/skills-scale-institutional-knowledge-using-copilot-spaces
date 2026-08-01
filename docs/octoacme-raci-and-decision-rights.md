# OctoAcme — RACI & Decision Rights

## Purpose
Clarify who is **Responsible**, **Accountable**, **Consulted**, and **Informed** for key project activities. Use this template to resolve ownership ambiguity, streamline handoffs, and agree escalation paths before work begins.

## RACI Key
| Letter | Meaning |
|--------|---------|
| **R** | **Responsible** — does the work |
| **A** | **Accountable** — owns the outcome; one person per activity |
| **C** | **Consulted** — provides input before the decision or action |
| **I** | **Informed** — notified of the decision or outcome |

---

## RACI Matrix — Core Project Activities

| Activity | Project Manager | Product Manager | Engineering Manager / Tech Lead | Developer | UX Designer | DevOps / Platform Eng | Security / Compliance | Data Analyst | Release Manager | Customer Support | Stakeholder / Sponsor |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Project initiation & charter | A | C | C | I | I | I | C | I | I | I | A |
| Backlog prioritization | C | A | C | C | C | I | C | C | I | C | C |
| Architecture & design decisions | C | C | A | R | C | C | C | I | I | I | I |
| Sprint planning | R | C | C | R | C | I | I | I | I | I | I |
| Feature implementation | I | I | C | A/R | C | C | C | I | I | I | I |
| UX design & usability validation | I | C | C | C | A/R | I | I | I | I | I | I |
| Security review & threat modelling | I | C | C | C | I | C | A/R | I | I | I | I |
| CI/CD pipeline management | I | I | C | C | I | A/R | C | I | I | I | I |
| Release readiness go/no-go | A | C | C | I | I | C | C | I | R | C | C |
| Production deployment | I | I | C | R | I | A/R | I | I | R | I | I |
| Release communications | C | C | I | I | I | I | I | I | A/R | R | I |
| Incident triage & response | R | I | C | R | I | R | C | I | C | I | I |
| Post-incident retrospective | A | I | C | R | I | R | C | I | C | I | I |
| Success metrics & KPI definition | I | A | C | I | C | I | I | R | I | I | C |
| Stakeholder status reporting | A/R | C | C | I | I | I | C | C | I | I | I |
| Escalation — Level 3 (business-impacting) | R | C | C | I | I | I | C | I | I | I | A |
| Retrospective facilitation | A/R | C | C | C | C | C | C | C | C | C | I |

> **Note:** Adapt this matrix for each project. Not all roles exist on every team — consolidate or leave blank as appropriate.

---

## Decision Rights Summary

### Project Initiation
- **Approve to start:** Stakeholder/Sponsor + Product Manager
- **Define scope:** Product Manager (accountable), consult Engineering Manager and Project Manager

### Technical Architecture
- **Final decision:** Engineering Manager / Tech Lead
- **Must consult:** Developers (impact), Security/Compliance Lead (risk), DevOps (operability)
- **Must inform:** Product Manager, Project Manager

### Scope Change
- **Minor scope adjustments** (within sprint): Product Manager with Engineering Manager agreement
- **Significant scope or timeline change:** Project Manager escalates to Stakeholder/Sponsor for approval
- **Budget change:** Stakeholder/Sponsor approval required

### Release Go/No-Go
- **Accountable:** Release Manager
- **Required approvers:** Engineering Manager/Tech Lead (technical), Security/Compliance Lead (security), Product Manager (scope/content)
- **Informed:** Stakeholder/Sponsor, Customer Support

### Security Incident
- **Lead:** Security/Compliance Lead
- **Immediate escalation:** Engineering Manager/Tech Lead + Project Manager
- **Stakeholder notification:** Project Manager within agreed SLA

---

## Escalation Path

```
Level 1: Team triage (daily standup / Slack)
Level 2: Project Manager + Product Manager alignment
Level 3: Engineering Manager / Tech Lead for technical blockers
           OR Security/Compliance Lead for security/compliance issues
Level 4: Stakeholder / Sponsor — business-impacting decisions or blocks
```

| Trigger | Owner | Escalation Target |
|---------|-------|-------------------|
| Technical blocker > 1 sprint | Developer → Engineering Manager | Project Manager |
| Scope creep > 10% | Product Manager | Stakeholder/Sponsor |
| Security finding (High/Critical) | Security Lead | Engineering Manager + Sponsor |
| Release deployment failure | Release Manager | DevOps + Engineering Manager |
| Customer-impacting incident | Customer Support | Project Manager → Stakeholder |

---

## Handoff Checklist

Use this checklist to confirm a clean handoff between lifecycle stages.

### Design → Development
- [ ] Designs reviewed and approved by Product Manager
- [ ] Acceptance criteria include usability and accessibility requirements (UX Designer confirmed)
- [ ] Telemetry/instrumentation requirements specified (Data Analyst confirmed)
- [ ] Security requirements documented (Security Lead confirmed)

### Development → QA / Testing
- [ ] Feature branch merged and CI passing
- [ ] Unit and integration tests written and passing
- [ ] Security scan passing (no new High/Critical findings)
- [ ] Developer demo or walkthrough completed for QA

### QA → Release
- [ ] All acceptance criteria verified (QA sign-off)
- [ ] Staging smoke tests passed
- [ ] Release notes drafted and reviewed by Product Manager
- [ ] Customer Support briefed on upcoming changes
- [ ] Security/Compliance sign-off obtained
- [ ] Rollback procedure confirmed with DevOps

### Post-Release
- [ ] Deployment verified by DevOps (post-deploy checks passing)
- [ ] Release communications sent (Release Manager)
- [ ] Success metrics baseline captured (Data Analyst)
- [ ] Retrospective scheduled (Project Manager)
