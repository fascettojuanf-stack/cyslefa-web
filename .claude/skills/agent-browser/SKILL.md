---
name: agent-browser
description: Browser automation CLI for AI agents. Use when the user needs to interact with websites, including navigating pages, filling forms, clicking buttons, taking screenshots, extracting data, testing web apps, or automating any browser task. Triggers include requests to "open a website", "fill out a form", "click a button", "take a screenshot", "scrape data from a page", "test this web app", "login to a site", "automate browser actions", or any task requiring programmatic web interaction. Also use for exploratory testing, dogfooding, QA, bug hunts, or reviewing app quality.
allowed-tools: Bash(agent-browser:*)
---

<!-- Source: https://github.com/vercel-labs/agent-browser/blob/main/skills/agent-browser/SKILL.md -->

# agent-browser

Fast browser automation CLI for AI agents. Chrome/Chromium via CDP with accessibility-tree snapshots and compact `@eN` element refs.

## Install (needs the user's approval)

The CLI is not preinstalled. If `agent-browser --version` fails, ask the user before installing:

```bash
npm i -g agent-browser
agent-browser install   # downloads Chrome; skip in cloud sessions if Chromium already exists
```

In Claude Code cloud sessions, Chromium is preinstalled at `/opt/pw-browsers/chromium`. Point agent-browser at it instead of downloading another browser (see `agent-browser skills get core` for the executable-path option).

## Start here

This file is a discovery stub, not the usage guide. Before running any `agent-browser` command, load the actual workflow content from the CLI:

```bash
agent-browser skills get core             # the loop, waits, common tasks, troubleshooting
```

The core guide ends with a table of references for detailed commands and flags. Use `agent-browser skills get core --full` only when you need every reference at once; it is several times larger.

## Specialized skills

```bash
agent-browser skills get electron          # Electron desktop apps
agent-browser skills get slack             # Slack workspace automation
agent-browser skills get dogfood           # Exploratory testing / QA / bug hunts
agent-browser skills get derive-client     # Record a HAR, derive an API client for a site
agent-browser skills get webmcp-gen        # Build and validate WebMCP tools for a page
agent-browser skills get modern-web-guidance  # Apply Modern Web Guidance, then verify the page
agent-browser skills get vercel            # Protected Vercel deployments and flag overrides
```

Run `agent-browser skills list` to see everything on the installed version.
