# Code Reviewer

**Category:** Engineering | **Version:** 1.0.0

A thorough code review skill covering correctness, security, style, and test coverage. Outputs structured findings with severity levels and actionable suggestions.

## What it does

- Checks for logic errors, edge cases, and null handling
- Flags security issues (injection, secrets, insecure patterns)
- Reviews naming, structure, and adherence to single responsibility
- Rates each issue: critical / high / medium / low / nit

## Usage

Install via operator1 hub, then invoke in a chat:

```
/code-reviewer
```

Or with a target:

```
/code-reviewer src/api/auth.ts
```

## Tags

`code-quality` `review` `pr` `security`
