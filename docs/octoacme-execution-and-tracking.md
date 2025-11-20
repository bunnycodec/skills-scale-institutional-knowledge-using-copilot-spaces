# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

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

### Role-owned quality gates
Specific quality gates are owned by designated roles to ensure clear accountability and expertise. For full role definitions and interactions, see [octoacme-roles-and-personas.md](./octoacme-roles-and-personas.md).

- **QA Lead:** Owns acceptance testing and feature validation gate
- **Security Liaison:** Owns security scanning and vulnerability assessment gate
- **SRE/DevOps:** Owns observability, monitoring, and infrastructure readiness gate
- **Tech Lead:** Owns code quality, architecture review, and technical design gate
- **Data Lead:** Owns instrumentation validation and metrics readiness gate (when applicable)

### Testing approach
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
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
- [ ] Role sign-offs for release readiness recorded (QA Lead, Security Liaison, SRE, Data Lead as applicable)
