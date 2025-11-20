# Release Checklist Template

**Release Name/Version:** _____________  
**Target Release Date:** _____________  
**Release Manager:** _____________

---

## Pre-release Checks

### Code Quality & Testing
- [ ] All PRs merged and linked to release milestone
- [ ] CI/CD pipeline passing (build, unit tests, integration tests)
- [ ] **QA Lead sign-off:** Acceptance tests completed  
  - **Signed by:** _____________ **Date:** _____________
- [ ] Code coverage meets team threshold
- [ ] End-to-end smoke tests passed on staging

### Security & Compliance
- [ ] Security scans (SAST/DAST) completed with no critical issues
- [ ] **Security Liaison review:** Security-impacting changes reviewed (if applicable)  
  - **Signed by:** _____________ **Date:** _____________
- [ ] Dependency vulnerabilities addressed
- [ ] Compliance requirements validated (if applicable)

### Infrastructure & Operations
- [ ] **SRE/DevOps sign-off:** Infrastructure changes reviewed and capacity validated  
  - **Signed by:** _____________ **Date:** _____________
- [ ] Deployment runbook reviewed and updated
- [ ] Rollback plan documented and tested
- [ ] Database migrations tested (if applicable)
- [ ] Configuration changes reviewed

### Observability & Monitoring
- [ ] **Data Lead verification:** Instrumentation and metrics validated (if metrics required)  
  - **Signed by:** _____________ **Date:** _____________
- [ ] Dashboards updated for new features
- [ ] Alerts configured for critical paths
- [ ] Log aggregation confirmed

### Documentation & Communication
- [ ] Release notes drafted and reviewed
- [ ] User-facing documentation updated
- [ ] Internal runbooks updated
- [ ] **Support Liaison notified:** Customer Success and Support teams briefed  
  - **Notified by:** _____________ **Date:** _____________

---

## Release Window & Communications

### Pre-release Communication
- [ ] Stakeholders notified of release window
- [ ] Maintenance window scheduled (if downtime expected)
- [ ] On-call rotation confirmed
- [ ] Incident response team on standby

### Deployment Steps
- [ ] Deployment window starts: **Time:** _____________
- [ ] Backup/snapshot created (if applicable)
- [ ] Deploy to staging environment
- [ ] Run smoke tests on staging
- [ ] Deploy to production (via automated pipeline or manual steps)
- [ ] Monitor deployment logs for errors

---

## Post-release Verification

### Functional Validation
- [ ] Smoke tests passed in production
- [ ] Key user flows verified
- [ ] New features accessible and functional
- [ ] No critical errors in logs

### Monitoring & Metrics
- [ ] Error rates within acceptable range
- [ ] Performance metrics stable (latency, throughput)
- [ ] Resource utilization normal (CPU, memory, database)
- [ ] User-facing metrics showing expected behavior

### Stakeholder Communication
- [ ] Release announcement sent to stakeholders
- [ ] Support team notified of go-live
- [ ] Customer-facing release notes published (if applicable)

---

## Rollback & Incident Response

### If Issues Arise
- [ ] Trigger incident response protocol
- [ ] Notify on-call and **Release Manager**
- [ ] Assess severity and decide: monitor, hotfix, or rollback
- [ ] Execute rollback to last known-good release (if necessary)
- [ ] Document incident timeline and root cause
- [ ] Schedule post-incident review

### Rollback Checklist
- [ ] Rollback initiated: **Time:** _____________
- [ ] Database rollback/restore (if applicable)
- [ ] Verify rollback completion
- [ ] Confirm system stability
- [ ] Notify stakeholders of rollback

---

## Final Sign-offs

### Release Approval
- [ ] **Tech Lead approval:** Code quality and technical readiness confirmed  
  - **Signed by:** _____________ **Date:** _____________
- [ ] **Release Manager sign-off:** All pre-release checks completed, release authorized  
  - **Signed by:** _____________ **Date:** _____________
- [ ] **Product Manager sign-off:** Release meets acceptance criteria and business requirements  
  - **Signed by:** _____________ **Date:** _____________

### Post-release Confirmation
- [ ] **Release Manager confirmation:** Release completed successfully, all verifications passed  
  - **Signed by:** _____________ **Date:** _____________
- [ ] Retrospective scheduled (if needed)
- [ ] Action items captured in project board

---

## Example: Cross-team Handoff Scenario

**Scenario:** A new payment feature requires security review, database migration, and customer support preparation.

1. **Dev Team → Security Liaison:** Submits security review request 5 days before release
2. **Security Liaison → Release Manager:** Provides sign-off after penetration testing
3. **SRE → Release Manager:** Confirms database migration tested in staging
4. **Release Manager → Support Liaison:** Shares release notes and demo 2 days before release
5. **Release Manager → All:** Coordinates go/no-go decision 1 hour before deployment window
