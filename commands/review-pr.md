---
name: review-pr
description: Review a GitHub PR with security, correctness, and style checks
emoji: "🔍"
category: engineering
user-command: true
model-invocation: true
long-running: true
args:
  - name: pr_url
    description: "GitHub PR URL or number (e.g. https://github.com/org/repo/pull/123 or 123)"
    required: true
tags: [code-review, github, pr, security]
---

Review the GitHub PR at {{pr_url}}.

## Instructions

1. Fetch the PR diff and metadata (title, description, linked issues)
2. Understand the intent — what is this PR trying to do?
3. Review each changed file:
   - Correctness: logic errors, edge cases, null handling
   - Security: injection, auth bypass, secrets exposure (OWASP Top 10)
   - Style: naming, structure, adherence to codebase conventions
   - Tests: are new code paths covered?
4. Check for breaking changes (API contracts, database migrations, config keys)
5. Summarize findings:
   - Overall verdict: Approve / Request Changes / Needs Discussion
   - List issues by severity: critical → high → medium → low → nit
   - Highlight any blocking issues clearly

## Output Format

```
## PR Review: <title>

**Verdict:** Approve | Request Changes | Needs Discussion

### Critical / Blocking
- file:line — issue — suggestion

### High
...

### Medium / Low / Nit
...

### Summary
<2-3 sentence overall assessment>
```
