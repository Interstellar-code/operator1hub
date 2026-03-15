---
name: deploy-check
description: Pre-deployment checklist — verify readiness before pushing to production
emoji: "🚀"
category: devops
user-command: true
model-invocation: true
long-running: false
args:
  - name: environment
    description: "Target environment (e.g. staging, production)"
    required: false
  - name: service
    description: "Service or component being deployed"
    required: false
tags: [deployment, checklist, production, readiness]
---

Run a pre-deployment readiness check{{#if service}} for {{service}}{{/if}}{{#if environment}} targeting {{environment}}{{/if}}.

## Checklist

### Code Quality
- [ ] All tests passing (unit, integration, e2e)
- [ ] No critical linting or type errors
- [ ] Code review approved (no unresolved blocking comments)
- [ ] No debug code, console.log, or TODO/FIXME in changed files

### Database & Data
- [ ] Migrations are backwards-compatible (old code can run against new schema)
- [ ] No destructive migrations (DROP, irreversible ALTER) without rollback plan
- [ ] Migration tested on staging with production-scale data
- [ ] No N+1 queries introduced in hot paths

### Security
- [ ] No secrets committed to code
- [ ] New endpoints have authentication/authorization
- [ ] Input validation on all user-facing inputs
- [ ] Dependencies up-to-date (no critical CVEs)

### Observability
- [ ] New code paths have logging for errors and key events
- [ ] Metrics/alerts added for new features
- [ ] Dashboards updated if new services added

### Deployment Safety
- [ ] Feature flags used for risky or large changes
- [ ] Rollback plan documented and tested
- [ ] Canary or staged rollout configured if high-risk
- [ ] On-call team notified of deployment window

### Post-Deploy Verification
- [ ] Smoke tests defined and ready to run
- [ ] Monitoring checked immediately after deploy
- [ ] Rollback trigger criteria defined (error rate threshold)

## Output

Report status of each category. Flag any unchecked items as blockers or warnings. Give a final **Go / No-Go** recommendation.
