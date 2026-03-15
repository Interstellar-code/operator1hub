# Operator1Hub

Curated registry of skills, agent personas, and commands for [operator1](https://github.com/Interstellar-code/operator1).

Ships as the **default built-in registry** — no setup required. Every item is tested and optimized before inclusion.

## Contents

| Type | Count |
|------|-------|
| Skills | 4 |
| Agents | 4 |
| Commands | 2 |
| Collections | 2 |

## Registry

The registry manifest is at [`registry.json`](./registry.json). operator1 fetches it directly via:

```
https://raw.githubusercontent.com/Interstellar-code/operator1hub/main/registry.json
```

## Structure

```
operator1hub/
├── registry.json          # manifest — single source of truth
├── skills/
│   ├── code-reviewer/
│   │   ├── SKILL.md
│   │   └── README.md
│   ├── security-audit/
│   ├── db-optimizer/
│   └── devops-automator/
├── agents/
│   ├── security-engineer.md
│   ├── sre-agent.md
│   ├── architect.md
│   └── technical-writer.md
├── commands/
│   ├── review-pr.md
│   └── deploy-check.md
└── collections/
    ├── engineering-essentials.json
    └── devops-starter.json
```

## License

MIT
