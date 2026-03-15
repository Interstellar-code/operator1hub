# Gmail MCP Server

Manage Gmail from AI agents — read, search, send, draft, and organize emails with automatic OAuth2 authentication.

## What it does

- **Read emails** — fetch messages by ID, list inbox, search by query
- **Send emails** — compose and send with subject, body, recipients, CC, BCC
- **Draft management** — create, list, update, and delete drafts
- **Label management** — list, apply, and remove Gmail labels
- **Thread operations** — read full threads, mark as read/unread, trash
- **Auto auth** — first-run OAuth2 flow; credentials cached locally

## Setup

Authenticate with your Google account on first use:

```bash
npx -y @gongrzhe/server-gmail-autoauth-mcp auth
```

A browser window will open for Google OAuth2. Once authorized, credentials are stored in `~/.gmail-mcp/`.

## Required Google Cloud setup

1. Create a project at [console.cloud.google.com](https://console.cloud.google.com)
2. Enable the **Gmail API**
3. Create OAuth2 credentials (Desktop app)
4. Download `credentials.json` → place at `~/.gmail-mcp/credentials.json`

## Transport

`stdio` — runs as a local subprocess via `npx`.

## Source

- npm: [`@gongrzhe/server-gmail-autoauth-mcp`](https://www.npmjs.com/package/@gongrzhe/server-gmail-autoauth-mcp)
- GitHub: [GongRzhe/Gmail-MCP-Server](https://github.com/GongRzhe/Gmail-MCP-Server)
