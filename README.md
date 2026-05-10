# Seojeom

Seojeom is a local-first desktop workspace for long-form fiction authoring.

It keeps your project, wiki, graph, and episode drafts on your machine, and lets external AI clients like Claude Code and Codex connect through MCP when you want AI help.

## What Seojeom is

- A desktop app for local project, wiki, graph, and draft authoring
- A reviewable workflow for graph and wiki changes
- A local-first workspace where your project state stays on your device
- An MCP-connected toolchain, not an AI SaaS that owns your source material

## Download

- Latest release: https://github.com/seojeom/seojeom/releases/latest
- Current Windows preview binary: https://github.com/seojeom/seojeom/releases/download/v0.1.0/seojeom.exe

## MCP

Seojeom MCP is published separately on npm:

- Package: https://www.npmjs.com/package/seojeom-mcp
- Public repo: https://github.com/seojeom/seojeom-mcp

Example install path:

```bash
npm exec --yes --package=seojeom-mcp seojeom-mcp -- --print-claude-onboarding
```

## Product Docs

- Desktop Project & Workbench PRD: `docs/desktop-project-workbench-prd.md`
- Desktop Authoring & Review PRD: `docs/desktop-authoring-review-prd.md`

## Product Principles

- Local-first: project state lives locally
- AI is optional: Claude Code / Codex can connect through MCP
- Mutation is reviewable: changes should go through proposal, approval, and apply
- Public distribution is binary-first: this repository is for releases, not full source exposure

## Status

This repository is the public release surface for Seojeom desktop binaries.

Current state:

- Windows preview binary is available
- MCP package is publicly installable
- Release/update metadata and broader platform coverage are still in progress
