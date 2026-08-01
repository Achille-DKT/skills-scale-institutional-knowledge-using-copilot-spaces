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

---

## Engineering Manager / Tech Lead

### Role Summary
The Engineering Manager (or Tech Lead where a separate management layer does not exist) owns technical direction, architectural alignment, and the overall engineering health of the delivery team. They bridge day-to-day execution and strategic technical decisions.

### Responsibilities
- Set and communicate technical standards, patterns, and architectural direction
- Review and approve significant design and architectural decisions
- Mentor and support developers through code reviews, 1:1s, and technical guidance
- Assess delivery feasibility and surface technical risks early
- Own hiring, team capacity planning, and engineering career development
- Co-own the Definition of Done for technical quality (test coverage, observability, security posture)

### Goals
- Maintain a healthy, high-velocity engineering team
- Prevent technical debt from accumulating unchecked
- Ensure architectural decisions are reversible or well-justified
- Reduce delivery risk through proactive technical risk management

### Typical Communication
- Weekly sync with Product Manager and Project Manager
- Architecture decision records (ADRs) or lightweight design docs
- Sprint planning participation for feasibility input
- Incident retrospectives as a technical owner

### Interaction with Existing Roles
- **Developers**: Primary coach and technical escalation point; approves architectural changes and unblocks high-complexity issues.
- **Product Managers**: Negotiates scope and trade-offs; translates technical constraints into product decisions.
- **Project Managers**: Surfaces technical risks and capacity concerns; collaborates on timeline adjustments.
- **DevOps/Platform Engineer**: Co-owns deployment safety and infrastructure evolution.
- **Security/Compliance Lead**: Partners on threat modelling and secure-by-default standards.

---

## UX Designer / Researcher

### Role Summary
UX Designers and Researchers ensure that features are usable, accessible, and grounded in real user needs. They translate research insights into validated designs that Developers can implement confidently.

### Responsibilities
- Conduct user research (interviews, usability tests, surveys) to inform product direction
- Create user flows, wireframes, and interactive prototypes
- Define and maintain the design system and interaction patterns
- Write user-centered acceptance criteria and usability heuristics
- Validate implementations against design intent before release
- Advocate for accessibility standards (WCAG compliance)

### Goals
- Ensure every shipped feature solves a real user problem
- Reduce post-release usability issues through early testing
- Maintain design consistency across the product surface
- Shorten feedback loops between user insight and backlog prioritization

### Typical Communication
- Design reviews and prototype walkthroughs with Product Managers and Developers
- Research read-outs shared with PMs and stakeholders
- Annotations and design files linked from backlog items
- Participation in sprint planning to flag design dependencies

### Interaction with Existing Roles
- **Developers**: Provides specifications, answers implementation questions, and validates designs in staging.
- **Product Managers**: Collaborates on discovery, user story framing, and acceptance criteria.
- **Project Managers**: Communicates design timeline dependencies and flags usability risks.
- **Stakeholder/Sponsor**: Presents research findings and design rationale at key review gates.

---

## DevOps / Platform Engineer

### Role Summary
DevOps and Platform Engineers own the reliability, security, and efficiency of the build, test, and deployment pipeline. They ensure the team can ship safely and quickly, with strong observability and rollback capability.

### Responsibilities
- Design, maintain, and improve CI/CD pipelines and deployment automation
- Manage environment parity (development, staging, production)
- Define and enforce deployment safety gates (automated tests, security scans, smoke tests)
- Implement and maintain observability tooling (logging, metrics, alerting, dashboards)
- Maintain infrastructure-as-code and platform documentation
- Lead incident triage for infrastructure and deployment-related failures
- Define and test rollback and disaster-recovery procedures

### Goals
- Achieve high deployment frequency with low change failure rate
- Minimize mean time to recovery (MTTR) for production incidents
- Ensure every release is observable, reversible, and auditable
- Enable Developers to ship confidently without requiring platform expertise

### Typical Communication
- Release planning sessions to align on deployment windows and readiness gates
- Incident on-call rotation and post-incident review participation
- Pipeline and infrastructure change announcements
- Runbook and operational documentation updates

### Interaction with Existing Roles
- **Developers**: Provides platform tooling guidance; reviews infrastructure changes in PRs; supports local environment setup.
- **Product Managers**: Communicates infrastructure constraints that affect release timelines.
- **Project Managers**: Confirms environment readiness and deployment window availability.
- **Engineering Manager/Tech Lead**: Aligns on platform evolution roadmap and technical standards.
- **Release Manager**: Executes deployment steps and confirms post-deploy verifications.
- **Security/Compliance Lead**: Enforces security scanning in pipelines; implements compliance controls.

---

## Security / Compliance Lead

### Role Summary
The Security/Compliance Lead ensures that the product is built and operated in line with security best practices and applicable compliance requirements. They integrate security earlier in the lifecycle (shift-left) and own the incident response security track.

### Responsibilities
- Perform threat modelling and risk assessments at planning and design stages
- Define and document security requirements and acceptance criteria for features
- Review code and architecture changes for security implications
- Run and interpret security scans (SAST, DAST, dependency audits); manage findings
- Maintain the security incident runbook and lead security incident response
- Track compliance obligations (e.g., SOC 2, GDPR, internal policies) and verify controls
- Advise teams on secure coding standards and data handling practices

### Goals
- Prevent security vulnerabilities from reaching production
- Maintain a current, actionable risk register for security and compliance items
- Ensure the team can respond quickly and effectively to security incidents
- Achieve and sustain required compliance certifications

### Typical Communication
- Security review checkpoints at initiation, design, and pre-release
- Findings reports shared with Engineering Manager and Project Manager
- Participation in release readiness gates as a security approver
- Post-incident security retrospectives

### Interaction with Existing Roles
- **Developers**: Provides secure coding guidance; reviews security-sensitive PRs.
- **Engineering Manager/Tech Lead**: Partners on security standards and architecture decisions.
- **DevOps/Platform Engineer**: Integrates security scanning into CI/CD; defines secrets management practices.
- **Project Managers**: Flags security risks in the risk register; confirms compliance gates before release.
- **Release Manager**: Acts as a required approver for security sign-off in the release checklist.
- **Stakeholder/Sponsor**: Reports on compliance posture and material security risks.

---

## Customer Support / Success Representative

### Role Summary
Customer Support and Success Representatives bring the voice of the customer into the delivery process. They surface recurring issues, adoption blockers, and post-release feedback to ensure the team ships features that customers can use successfully.

### Responsibilities
- Collect and synthesize customer issue trends and feature requests from support channels
- Share customer sentiment and usage patterns with Product Managers and Project Managers
- Prepare support documentation, FAQs, and training materials for upcoming releases
- Validate release communications and change summaries for customer clarity
- Coordinate post-release feedback loops and report adoption metrics
- Escalate critical customer-impacting issues to the appropriate team

### Goals
- Reduce customer-impacting issues caused by insufficient communication or poor usability
- Enable support teams to handle new features confidently from day one
- Close the feedback loop between customers and the delivery team

### Typical Communication
- Participation in release planning to flag support readiness needs
- Pre-release walkthroughs to prepare support documentation
- Post-release feedback summaries shared with PM and PdM
- Escalation of high-impact customer issues via the defined escalation path

### Interaction with Existing Roles
- **Product Managers**: Provides customer insight for prioritization; reviews acceptance criteria from a user perspective.
- **Project Managers**: Raises communication readiness as a release dependency.
- **Developers**: Requests clarification on behavioural changes that affect customer workflows.
- **Release Manager**: Coordinates customer-facing release communications and support handoff.

---

## Data Analyst / BI Partner

### Role Summary
Data Analysts and BI Partners enable evidence-based decision-making by defining metrics, building instrumentation, and analysing outcomes. They ensure the team can measure whether shipped features achieve their intended impact.

### Responsibilities
- Collaborate with Product Managers to define outcome metrics and KPIs
- Specify telemetry and instrumentation requirements for new features
- Build and maintain dashboards and reports for delivery and product metrics
- Analyse post-release data to validate hypotheses and inform future iterations
- Identify data quality issues and work with Developers to resolve them
- Support prioritization decisions with data from production and user behaviour

### Goals
- Ensure every key feature has measurable, trackable success criteria
- Shorten the feedback loop between shipping and learning
- Improve data quality and reliability across the product
- Enable self-serve analytics for product and delivery teams

### Typical Communication
- Participation in planning to define instrumentation requirements as acceptance criteria
- Dashboard and metric reviews in sprint demos or weekly syncs
- Post-release analysis reports shared with PMs and stakeholders
- Data quality incident escalations to Developers and Engineering Manager

### Interaction with Existing Roles
- **Product Managers**: Defines KPIs together; validates that success metrics are measurable before features are built.
- **Developers**: Specifies telemetry events and data schema requirements during design.
- **Project Managers**: Provides metrics to support project health reporting and retrospectives.
- **Stakeholder/Sponsor**: Presents outcome analysis at milestone or quarterly reviews.

---

## Release Manager

### Role Summary
The Release Manager coordinates all activities required to safely deploy a release to production. They act as the single point of accountability for release readiness, change window management, and cross-team release communication.

### Responsibilities
- Maintain the release calendar and coordinate change windows with stakeholders
- Compile and own the release checklist, confirming all gates are met before deployment
- Coordinate go/no-go decisions across Engineering, QA, Security, and Support
- Manage release communications — internal announcements and external release notes
- Oversee rollback decisions and coordinate incident response for release-related failures
- Maintain a release log capturing deployment history, outcomes, and follow-up actions

### Goals
- Reduce release risk through thorough readiness validation
- Ensure all approvers are aligned before any deployment proceeds
- Maintain a clear audit trail for every production change
- Accelerate release cadence without sacrificing reliability

### Typical Communication
- Pre-release readiness meetings with all approving roles
- Release calendar updates shared with PM, DevOps, and stakeholders
- Go/no-go confirmation documented and distributed before deployment
- Post-release retrospective notes and follow-up tracking

### Interaction with Existing Roles
- **DevOps/Platform Engineer**: Confirms pipeline readiness and executes deployment steps.
- **Security/Compliance Lead**: Obtains security sign-off as part of the release gate.
- **Product Managers**: Confirms scope and release notes accuracy.
- **Project Managers**: Aligns release date with project milestones and stakeholder expectations.
- **Customer Support/Success Representative**: Coordinates support readiness and customer communications.
- **Stakeholder/Sponsor**: Presents go/no-go status and obtains final approval for major releases.

---

## Stakeholder / Sponsor

### Role Summary
Stakeholders and Sponsors provide strategic direction, funding authority, and organisational alignment for projects. They make or ratify high-impact decisions, remove organisational blockers, and hold accountability for business outcomes.

### Responsibilities
- Approve project initiation, scope changes, and major investment decisions
- Provide business context and strategic priorities that guide trade-off decisions
- Remove blockers that cannot be resolved at the delivery team level
- Review and accept key deliverables at defined project gates
- Ensure organisational readiness for change (staffing, communications, process change)
- Hold accountability for business outcome metrics beyond the project lifecycle

### Goals
- Ensure projects deliver measurable business value aligned with strategic goals
- Minimise organisational risk through clear decision rights and timely escalations
- Maintain confidence among external stakeholders (customers, regulators, leadership)

### Typical Communication
- Monthly or milestone-based project status briefings
- Formal decision requests (scope change, budget, go/no-go) with clear options and recommendations
- Escalation notifications for material risks or blockers
- Post-project outcome review and lessons-learned summary

### Decision Rights
- **Approve**: Project go/no-go, major scope or budget changes, and final production release for major versions.
- **Consult**: Technical architecture decisions with significant business risk; compliance posture changes.
- **Inform**: Sprint velocity, minor scope adjustments, and operational metrics.

### Interaction with Existing Roles
- **Product Managers**: Aligns on roadmap priorities and approves business case changes.
- **Project Managers**: Receives escalations; provides decisions at Level 3 escalation.
- **Engineering Manager/Tech Lead**: Reviews major architectural risks with business impact.
- **Security/Compliance Lead**: Receives compliance posture updates and approves risk acceptance decisions.
- **Release Manager**: Provides final approval gate for major version releases.

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- The **Interaction with Existing Roles** subsections make handoffs, decision rights, and collaboration points explicit for each persona.

