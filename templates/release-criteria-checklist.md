# Release Criteria Checklist

## Release Information
- **Release Name/Version:**
- **Release Type:** [ ] Patch [ ] Minor [ ] Major
- **Target Release Date:**
- **Release Manager:**
- **Quality Assurance Lead:**
- **Project Manager:**

## Purpose
This checklist ensures all release criteria are met before deploying to production. Use it to verify release readiness and minimize production risks.

---

## Pre-Development Release Criteria

### Requirements and Planning
- [ ] All features in scope have clear acceptance criteria
- [ ] User stories have been prioritized and estimated
- [ ] Definition of Done (DoD) is documented and agreed upon
- [ ] Release goals and success metrics are defined
- [ ] Rollback plan is documented
- [ ] Release notes template is prepared

### Infrastructure and Environment
- [ ] Staging environment mirrors production configuration
- [ ] Deployment pipeline is tested and functional
- [ ] Monitoring and alerting are configured
- [ ] Database migration scripts are prepared (if applicable)
- [ ] Feature flags are configured (if using feature toggling)

---

## Development Phase Release Criteria

### Code Quality
- [ ] All code follows project coding standards and conventions
- [ ] Code reviews completed for all PRs with required approvals
- [ ] No critical or high-severity linting errors
- [ ] Technical debt is documented and tracked
- [ ] Code coverage meets minimum threshold (specify: ___%)

### Testing - Unit Tests
- [ ] Unit tests exist for all new business logic
- [ ] All unit tests pass successfully
- [ ] Test coverage meets team standards (minimum ___%)
- [ ] Edge cases and error conditions are tested
- [ ] Mock/stub dependencies are properly configured

### Testing - Integration Tests
- [ ] Integration tests cover key system interactions
- [ ] All integration tests pass successfully
- [ ] API contract tests pass (if applicable)
- [ ] Database migrations tested in non-production environment
- [ ] Third-party integrations validated

### Testing - End-to-End Tests
- [ ] Critical user flows have E2E test coverage
- [ ] All E2E smoke tests pass successfully
- [ ] Cross-browser testing completed (if applicable)
- [ ] Mobile responsiveness verified (if applicable)
- [ ] Performance benchmarks meet requirements

### Security and Compliance
- [ ] Security scanning completed with no critical vulnerabilities
- [ ] Dependency vulnerabilities addressed or documented
- [ ] Authentication and authorization tested
- [ ] Input validation and sanitization verified
- [ ] Sensitive data handling reviewed
- [ ] Compliance requirements met (GDPR, SOC2, etc.)

---

## Pre-Release Validation Criteria

### Quality Assurance Sign-Off
- [ ] All acceptance criteria validated by QA team
- [ ] Manual testing completed for critical features
- [ ] Exploratory testing completed
- [ ] Regression testing passed
- [ ] Known issues documented and prioritized
- [ ] No critical or high-priority bugs outstanding
- [ ] Bug fixes verified and retested

### Performance and Scalability
- [ ] Load testing completed (if applicable)
- [ ] Performance benchmarks meet requirements
- [ ] Response time within acceptable limits
- [ ] Resource utilization is acceptable (CPU, memory, storage)
- [ ] Database query performance optimized

### Documentation
- [ ] User-facing documentation updated
- [ ] API documentation updated (if applicable)
- [ ] Release notes completed with all changes
- [ ] Known issues and workarounds documented
- [ ] Deployment runbook updated
- [ ] Rollback procedure documented

### Stakeholder Approval
- [ ] Product Manager sign-off on features
- [ ] Project Manager sign-off on release readiness
- [ ] Quality Assurance Lead sign-off on quality
- [ ] Technical Lead sign-off on architecture and security
- [ ] Stakeholder demo/review completed
- [ ] Customer-facing teams briefed (support, sales, success)

---

## Deployment Readiness Criteria

### Pre-Deployment Checklist
- [ ] Deployment window scheduled and communicated
- [ ] On-call rotation confirmed and briefed
- [ ] Maintenance window notification sent (if applicable)
- [ ] Backup or database snapshot completed
- [ ] Deployment scripts tested in staging
- [ ] Environment variables and configurations verified
- [ ] SSL certificates valid and up-to-date (if applicable)

### Deployment Process
- [ ] Deploy to staging environment successfully
- [ ] Run smoke tests in staging
- [ ] Verify staging environment health
- [ ] Obtain final go/no-go decision
- [ ] Execute production deployment
- [ ] Monitor deployment progress and logs

### Post-Deployment Verification
- [ ] Application starts successfully
- [ ] Health check endpoints responding
- [ ] Critical user flows tested in production
- [ ] Database migrations completed successfully
- [ ] No error spikes in monitoring dashboards
- [ ] Performance metrics within normal range
- [ ] Key business metrics verified (if applicable)

---

## Release Communication Criteria

### Pre-Release Communication
- [ ] Release announcement sent to stakeholders
- [ ] Release notes published and accessible
- [ ] Customer-facing teams notified and trained
- [ ] Known issues communicated proactively
- [ ] Support team prepared with FAQs

### Post-Release Communication
- [ ] Deployment success confirmation sent
- [ ] Release announcement published (blog, email, etc.)
- [ ] Internal teams notified of completion
- [ ] Monitoring dashboards shared with stakeholders
- [ ] Post-release support contact established

---

## Post-Release Validation Criteria

### Monitoring and Observability (First 24 Hours)
- [ ] Error rates monitored and within normal limits
- [ ] Performance metrics stable
- [ ] User traffic patterns normal
- [ ] No critical alerts triggered
- [ ] Database performance stable
- [ ] API response times acceptable

### Customer Impact Assessment
- [ ] Customer feedback monitored
- [ ] Support ticket volume normal
- [ ] User adoption metrics tracked
- [ ] No critical customer-reported issues
- [ ] Success metrics trending positively

### Team Validation
- [ ] All team members confirm no critical issues
- [ ] On-call handoff completed with context
- [ ] Lessons learned captured for retrospective
- [ ] Action items documented for follow-up

---

## Rollback Criteria (When to Rollback)

Consider rollback if any of the following occur:
- [ ] Critical functionality is broken
- [ ] Error rates exceed acceptable thresholds
- [ ] Performance degrades significantly
- [ ] Security vulnerability discovered
- [ ] Data integrity issues detected
- [ ] Multiple high-priority customer issues reported
- [ ] Monitoring shows concerning trends

### Rollback Process
- [ ] Incident declared and stakeholders notified
- [ ] Rollback procedure executed per runbook
- [ ] Health verification after rollback
- [ ] Post-rollback communication sent
- [ ] Root cause analysis scheduled

---

## Release Sign-Off

### Required Approvals Before Release
| Role | Name | Sign-Off | Date |
|------|------|----------|------|
| Quality Assurance Lead | | [ ] Approved | |
| Technical Lead | | [ ] Approved | |
| Product Manager | | [ ] Approved | |
| Project Manager | | [ ] Approved | |
| Security Review (if required) | | [ ] Approved | |

### Final Go/No-Go Decision
- [ ] **GO** - All criteria met, proceed with deployment
- [ ] **NO-GO** - Criteria not met, address issues before release

**Decision Date:** _______________
**Decision Maker:** _______________
**Rationale:**
[Explain the decision and any conditions]

---

## Post-Release Retrospective

### Schedule Post-Release Review
- [ ] Retrospective meeting scheduled
- [ ] Invite all key stakeholders and team members
- [ ] Prepare release metrics and feedback

### Key Questions to Address:
- What went well during this release?
- What could be improved?
- Were all release criteria appropriate and sufficient?
- What surprised us during or after release?
- What should we do differently next time?

### Action Items
[Document improvements to process, criteria, or tooling]

---

## Release Criteria Exceptions

If any criteria cannot be met, document exceptions here:

| Criterion Not Met | Justification | Risk Assessment | Mitigation Plan | Approved By |
|-------------------|---------------|-----------------|-----------------|-------------|
| | | | | |

---

## Release Types - Specific Criteria

### Patch Release (Hotfix)
Additional criteria for urgent fixes:
- [ ] Impact limited to specific bug fix
- [ ] Change is minimal and well-isolated
- [ ] Testing focused on affected area
- [ ] Expedited approval process followed
- [ ] Communication includes urgency context

### Minor Release
Additional criteria for incremental features:
- [ ] Backward compatible with previous version
- [ ] No breaking changes to APIs or integrations
- [ ] Migration path documented (if needed)
- [ ] Feature flags used for gradual rollout (if applicable)

### Major Release
Additional criteria for significant changes:
- [ ] Breaking changes documented clearly
- [ ] Migration guide provided to users
- [ ] Extended testing period completed
- [ ] Customer communication plan executed
- [ ] Support resources allocated for transition
- [ ] Rollback strategy includes data migration reversal

---

**Related Documentation:**
- [Release & Deployment Guide](../docs/octoacme-release-and-deployment.md)
- [Execution & Tracking](../docs/octoacme-execution-and-tracking.md)
- [Risk Management & Communication](../docs/octoacme-risks-and-communication.md)
- [Roles and Personas - Quality Assurance Lead](../docs/octoacme-roles-and-personas.md#quality-assurance-lead)
