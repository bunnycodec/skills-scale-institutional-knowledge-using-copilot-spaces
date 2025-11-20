# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Manager Role
The **Release Manager** (or Release Coordinator) owns the end-to-end release process, ensuring all pre-release gates are met, coordinating deployment activities, and confirming post-release verification. See [octoacme-roles-and-personas.md](./octoacme-roles-and-personas.md) for full role definition and interactions with other team members.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements

All pre-release requirements must be validated and signed off by the appropriate role owner before deployment:

- All acceptance criteria met and PRs merged
- Passing CI and security scans
- **QA Lead sign-off required:** All acceptance tests completed and passed
- **Security Liaison review required (if security-impacting):** Security scans reviewed, vulnerabilities addressed, and secure practices validated
- **SRE/DevOps sign-off required:** Infrastructure changes reviewed, capacity validated, and deployment runbook updated
- **Data Lead instrumentation verification required (if metrics required):** Analytics instrumentation implemented and validated in staging
- Release notes drafted and reviewed
- Rollback / mitigation plan documented and tested
- Smoke tests prepared and validated in staging
- **Release Manager runbook check:** All checklists and sign-offs confirmed complete

For a comprehensive, reusable checklist with all sign-off fields, see [Release Checklist Template](./templates/release-checklist.md).

## Deployment Checklist

**Note:** Use the [Release Checklist Template](./templates/release-checklist.md) for a comprehensive, ownerable checklist with pre-release, deployment, and post-release sections.

- [ ] **Release Manager:** Deployment window scheduled and communicated (if needed)
- [ ] **SRE/DevOps:** Backup or snapshot created (if applicable)
- [ ] **Release Manager + QA Lead:** Deploy to staging and run smoke tests
- [ ] **Release Manager + SRE:** Deploy to production (automated pipeline preferred)
- [ ] **QA Lead + SRE:** Run post-deploy verifications
- [ ] **Release Manager:** Announce release to stakeholders and support
- [ ] **Release Manager:** Confirm all sign-offs and close release

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
