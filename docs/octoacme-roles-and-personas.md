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

## Additional personas & cross-functional roles

### Release Manager / Release Coordinator

#### Role Summary
Release Managers coordinate and oversee the end-to-end release process, ensuring all pre-release gates are met, deployment activities are executed smoothly, and post-release verification is completed. They serve as the central point of accountability for production deployments.

#### Responsibilities
- Own the release schedule and coordinate deployment windows
- Ensure all pre-release sign-offs are collected (QA, Security, SRE, Data)
- Facilitate go/no-go decisions before deployment
- Coordinate rollback procedures if issues arise
- Maintain release runbooks and checklists
- Communicate release status to stakeholders and support teams

#### Goals
- Execute zero-downtime, low-risk deployments
- Ensure cross-team readiness and coordination
- Maintain clear audit trail of release approvals

#### Typical Communication
- Pre-release checklist reviews with cross-functional teams
- Release status updates to stakeholders
- Post-release retrospectives and incident debriefs

#### Interactions with Other Roles
- **PM/PdM:** Aligns on release scope, priorities, and communication plans
- **Developers:** Confirms code freeze, PRs merged, and deployment readiness
- **QA Lead:** Obtains acceptance sign-off before deployment
- **SRE/DevOps:** Coordinates infrastructure changes and monitors deployment health
- **Security Liaison:** Ensures security reviews are completed for high-risk changes
- **Support Liaison:** Briefs support teams on new features and known issues

#### Example Interaction Scenario
*Two days before a major release, the Release Manager convenes a readiness review. QA Lead confirms all acceptance tests passed. Security Liaison flags a minor vulnerability in a non-critical path and approves with a follow-up ticket. SRE confirms staging deployment succeeded. Release Manager collects all sign-offs, schedules the production window, and notifies Support and stakeholders.*

---

### Tech Lead / Engineering Manager

#### Role Summary
Tech Leads provide technical direction, architectural oversight, and mentorship to the development team. They balance hands-on coding with leadership responsibilities, ensuring technical quality and team productivity.

#### Responsibilities
- Define technical architecture and design patterns
- Review and approve high-impact code changes
- Mentor developers and conduct technical coaching
- Identify and mitigate technical risks and debt
- Collaborate with PM/PdM on feasibility and estimates
- Represent engineering in cross-functional planning

#### Goals
- Maintain high code quality and architectural consistency
- Enable team productivity and technical growth
- Reduce technical debt and long-term maintenance costs

#### Typical Communication
- Architecture design docs and technical RFCs
- Code review feedback and technical guidance
- Engineering sync-ups and team retrospectives

#### Interactions with Other Roles
- **PM/PdM:** Advises on technical feasibility, estimates, and trade-offs
- **Developers:** Provides technical mentorship and code review
- **QA Lead:** Collaborates on test strategy and quality gates
- **Release Manager:** Approves release readiness from a technical perspective
- **DevOps/SRE:** Aligns on infrastructure, observability, and scalability

#### Example Interaction Scenario
*During sprint planning, the Product Manager proposes a new feature requiring real-time notifications. The Tech Lead evaluates options (WebSockets vs. polling), estimates complexity, identifies a risk around connection scaling, and proposes a phased rollout with observability. They work with SRE to plan load testing before release.*

---

### QA Lead / Test Engineer

#### Role Summary
QA Leads design and execute test strategies to ensure software quality and reliability. They define acceptance criteria, manage test automation, and provide the final quality sign-off before releases.

#### Responsibilities
- Develop and maintain test plans and test cases
- Execute manual and automated testing (functional, regression, performance)
- Verify acceptance criteria for all features
- Identify and triage bugs and quality issues
- Provide go/no-go quality assessment for releases
- Collaborate on Definition of Done and quality standards

#### Goals
- Ensure features meet acceptance criteria and quality standards
- Reduce production defects and customer-impacting bugs
- Improve test coverage and automation efficiency

#### Typical Communication
- Test plans and quality reports
- Bug triage and prioritization discussions
- Sign-off confirmations for release readiness

#### Interactions with Other Roles
- **PM/PdM:** Clarifies acceptance criteria and validates user scenarios
- **Developers:** Reports bugs, verifies fixes, and reviews testability
- **Release Manager:** Provides quality sign-off before deployment
- **Tech Lead:** Aligns on test strategy and automation architecture
- **Support Liaison:** Shares known issues and workarounds for customer communication

#### Example Interaction Scenario
*A week before release, the QA Lead runs acceptance tests on staging and discovers a critical regression in the checkout flow. They immediately file a high-priority bug, notify the Tech Lead and Release Manager, and block the release. Developers fix the issue, QA re-tests and signs off, and the release proceeds.*

---

### DevOps / SRE (Operations Owner)

#### Role Summary
DevOps/SRE engineers own infrastructure reliability, deployment automation, and operational observability. They ensure systems are scalable, resilient, and maintainable in production.

#### Responsibilities
- Build and maintain CI/CD pipelines and deployment automation
- Monitor system health, performance, and availability
- Manage infrastructure provisioning and scaling
- Respond to incidents and perform root cause analysis
- Implement observability (metrics, logs, traces, alerts)
- Plan and execute disaster recovery and rollback procedures

#### Goals
- Achieve high availability and low mean time to recovery (MTTR)
- Automate deployment and operational tasks
- Ensure systems are observable and debuggable

#### Typical Communication
- Incident response and post-mortems
- Infrastructure design docs and runbooks
- On-call handoffs and operational reviews

#### Interactions with Other Roles
- **Developers:** Provides deployment tooling, reviews infrastructure code
- **Release Manager:** Coordinates deployments, confirms infrastructure readiness
- **Tech Lead:** Aligns on scalability, observability, and architecture
- **QA Lead:** Collaborates on performance and load testing
- **Security Liaison:** Implements security controls and audit logging

#### Example Interaction Scenario
*During a release, the SRE monitors deployment metrics and notices elevated error rates in the API gateway. They alert the Release Manager and recommend a rollback. After rollback, they work with developers to identify a misconfigured rate limit, apply a fix, and successfully redeploy.*

---

### Security & Compliance Liaison

#### Role Summary
Security Liaisons champion security best practices throughout the development lifecycle. They review code for vulnerabilities, ensure compliance with security policies, and lead incident response for security events.

#### Responsibilities
- Conduct security reviews and threat modeling
- Review code and infrastructure for vulnerabilities
- Manage security scanning tools (SAST, DAST, dependency scans)
- Ensure compliance with security policies and regulatory requirements
- Lead security incident response and post-incident reviews
- Educate the team on secure coding practices

#### Goals
- Minimize security vulnerabilities and attack surface
- Ensure compliance with security and privacy regulations
- Maintain security awareness across the team

#### Typical Communication
- Security review reports and recommendations
- Threat models and risk assessments
- Security incident notifications and retrospectives

#### Interactions with Other Roles
- **Developers:** Reviews code for security issues, provides secure coding guidance
- **Release Manager:** Provides security sign-off for security-impacting releases
- **Tech Lead:** Advises on secure architecture and design patterns
- **DevOps/SRE:** Collaborates on infrastructure security and access controls
- **Compliance Advisors:** Ensures regulatory requirements are met

#### Example Interaction Scenario
*A new feature collects user payment data. The Security Liaison conducts a threat model, identifies PCI-DSS requirements, recommends tokenization, and reviews the implementation. They approve the feature after validating encryption, access controls, and audit logging are in place.*

---

### UX / Researcher / Designer

#### Role Summary
UX Designers create user-centered designs, conduct usability research, and ensure products are intuitive and accessible. They translate user needs into wireframes, prototypes, and design specifications.

#### Responsibilities
- Conduct user research and usability testing
- Design wireframes, mockups, and interactive prototypes
- Define user flows and interaction patterns
- Ensure accessibility and inclusive design standards
- Collaborate with developers on design implementation
- Validate designs with users and iterate based on feedback

#### Goals
- Create intuitive, delightful user experiences
- Ensure accessibility for all users
- Validate designs with real user feedback

#### Typical Communication
- Design mockups and interactive prototypes
- Usability testing reports and insights
- Design reviews and feedback sessions

#### Interactions with Other Roles
- **PM/PdM:** Translates product requirements into user flows and designs
- **Developers:** Collaborates on design implementation and feasibility
- **QA Lead:** Partners on usability testing and acceptance criteria
- **Accessibility Advisors:** Ensures designs meet accessibility standards
- **Support Liaison:** Gathers user feedback on pain points

#### Example Interaction Scenario
*The Product Manager requests a redesign of the onboarding flow. The UX Designer conducts user interviews, identifies friction points, creates wireframes, and tests prototypes with 5 users. They iterate based on feedback, finalize designs, and work with developers to implement and validate the new flow.*

---

### Data / Measurement Lead

#### Role Summary
Data Leads define success metrics, implement instrumentation, and analyze product performance. They ensure data-driven decision-making and measure the impact of product changes.

#### Responsibilities
- Define KPIs and success metrics for features and initiatives
- Implement analytics instrumentation and event tracking
- Build dashboards and reports for stakeholders
- Analyze user behavior and product performance
- Validate data quality and instrumentation correctness
- Provide insights to inform prioritization and iteration

#### Goals
- Enable data-driven decision-making across the team
- Measure and communicate product impact
- Ensure instrumentation is accurate and actionable

#### Typical Communication
- Metrics dashboards and analysis reports
- Experiment design and A/B test results
- Instrumentation specifications and reviews

#### Interactions with Other Roles
- **PM/PdM:** Defines success metrics and interprets data insights
- **Developers:** Specifies instrumentation requirements and validates implementation
- **Release Manager:** Confirms metrics and dashboards are ready before release
- **QA Lead:** Validates event tracking in testing environments
- **DevOps/SRE:** Collaborates on observability and monitoring infrastructure

#### Example Interaction Scenario
*Before a feature launch, the Data Lead works with the Product Manager to define conversion metrics and create a dashboard. They write instrumentation specs, review the developer's implementation in a PR, and validate events in staging. Post-launch, they analyze results and report that the feature increased conversions by 12%.*

---

### Support / Customer Success Liaison

#### Role Summary
Support Liaisons bridge the gap between customers and the product team. They gather feedback, communicate feature changes, and ensure customer-facing teams are prepared for new releases.

#### Responsibilities
- Communicate release notes and feature changes to support teams
- Gather and triage customer feedback and feature requests
- Escalate critical customer issues to engineering
- Document known issues and workarounds
- Train support teams on new features
- Track customer sentiment and satisfaction

#### Goals
- Ensure seamless customer experience during releases
- Reduce support escalations and resolution time
- Amplify customer voice in product planning

#### Typical Communication
- Release notes and feature summaries for support teams
- Customer feedback and escalation reports
- Training sessions and knowledge base updates

#### Interactions with Other Roles
- **PM/PdM:** Shares customer feedback and feature requests
- **Release Manager:** Receives advance notice of releases and known issues
- **QA Lead:** Learns about test coverage and potential edge cases
- **Developers:** Escalates critical bugs and gathers technical context
- **UX Designer:** Provides user feedback on usability and pain points

#### Example Interaction Scenario
*The Support Liaison receives several tickets about a confusing checkout flow. They analyze the feedback, document common patterns, and share insights with the Product Manager and UX Designer. The team prioritizes a redesign, and the Support Liaison later trains the support team on the improved flow before release.*

---

### Business Owner / Sponsor Representative

#### Role Summary
Business Owners represent executive stakeholders and provide strategic direction. They secure funding, align initiatives with business goals, and make high-level prioritization decisions.

#### Responsibilities
- Define business objectives and success criteria
- Secure budget and resources for initiatives
- Approve scope changes and major trade-offs
- Review progress and hold teams accountable to commitments
- Remove organizational blockers and escalate risks
- Communicate outcomes to executive leadership

#### Goals
- Align product investments with business strategy
- Maximize return on investment (ROI)
- Ensure organizational alignment and buy-in

#### Typical Communication
- Executive briefings and business reviews
- Budget and resource allocation decisions
- Strategic roadmap discussions

#### Interactions with Other Roles
- **PM/PdM:** Aligns on strategic priorities and business outcomes
- **Project Manager:** Reviews project status, risks, and budget
- **Release Manager:** Approves release timing for business-critical launches
- **Tech Lead:** Discusses technical investments and trade-offs
- **Support Liaison:** Monitors customer satisfaction and escalations

#### Example Interaction Scenario
*The Business Owner reviews quarterly roadmap and identifies a strategic opportunity to expand into a new market. They allocate budget, assign a PM to lead discovery, and set success metrics. They review progress monthly, approve a scope expansion mid-project, and present results to the executive team.*

---

### Accessibility / Legal / Privacy Advisors

#### Role Summary
Advisors provide specialized guidance on accessibility standards, legal compliance, and privacy regulations. They ensure products meet regulatory requirements and are inclusive for all users.

#### Responsibilities
- Review features for accessibility compliance (WCAG, ADA)
- Ensure legal and regulatory compliance (GDPR, CCPA, etc.)
- Review privacy policies and data handling practices
- Conduct privacy impact assessments for data collection
- Advise on terms of service, contracts, and legal risks
- Provide sign-off on compliance-sensitive releases

#### Goals
- Ensure legal and regulatory compliance
- Minimize legal and reputational risk
- Ensure products are accessible to all users

#### Typical Communication
- Compliance review reports and recommendations
- Privacy impact assessments
- Legal risk assessments and guidance

#### Interactions with Other Roles
- **PM/PdM:** Advises on compliance requirements and risks
- **UX Designer:** Ensures designs meet accessibility standards
- **Developers:** Reviews implementation for compliance
- **Security Liaison:** Collaborates on data protection and privacy
- **Release Manager:** Provides compliance sign-off before release

#### Example Interaction Scenario
*A new feature collects location data from users. The Privacy Advisor conducts a privacy impact assessment, identifies GDPR consent requirements, recommends explicit opt-in language, and reviews the implementation. They sign off after confirming data retention policies and user rights (deletion, export) are implemented.*

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

