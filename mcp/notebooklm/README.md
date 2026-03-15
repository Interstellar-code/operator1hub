# NotebookLM MCP Server

Query Google NotebookLM from AI agents — grounded, citation-backed answers from your personal knowledge base. Zero hallucinations, just your sources.

## What it does

- **Query notebooks** — ask questions and get answers grounded in your NotebookLM sources
- **Manage notebooks** — create, list, and organize notebooks
- **Manage sources** — add URLs, PDFs, text, and Google Docs as sources
- **Studio content** — generate audio overviews, briefing docs, study guides, and FAQs
- **Persistent auth** — authenticate once, works across all MCP clients

## Setup

First run the auth command to authenticate with your Google account:

```bash
npx -y notebooklm-mcp@latest auth
```

Follow the OAuth2 flow in your browser. Credentials are stored locally.

## Transport

`stdio` — runs as a local subprocess via `npx`.

## Source

- npm: [`notebooklm-mcp`](https://www.npmjs.com/package/notebooklm-mcp)
- GitHub: [PleasePrompto/notebooklm-mcp](https://github.com/PleasePrompto/notebooklm-mcp)
