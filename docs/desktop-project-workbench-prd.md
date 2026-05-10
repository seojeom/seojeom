# Seojeom Desktop Project & Workbench PRD

## Purpose

This document defines the practical product contract for project entry, re-entry, workspace persistence, navigation, degraded-state truth, and local artifact authority in Seojeom Desktop.

## Product Goal

Users should be able to create a project, return to it later, and resume the same working context without relying on cloud state or AI availability.

## Scope

- project creation and open flow
- recent and pinned project re-entry
- workspace shell and restore
- navigation and resource discovery
- degraded-state visibility
- local artifact authority and recovery

## Core Requirements

### 1. Project Bootstrap And Re-entry

- Users can create a project without signing in.
- `Open folder` must inspect `.seojeom/` first.
- legacy `.ainovel/`-only folders must surface as migration candidates.
- recent and pinned projects must show name, path, last-opened time, and health state.
- missing-path, recovery-needed, and migration-needed states must never be hidden.

### 2. Workspace Shell And Persistence

- workspace state must be stored per project
- reopen must restore tabs, active resource, pane visibility, and layout
- invalid restore payloads must fall back safely instead of blocking the whole app
- closed panes must remain discoverable and recoverable

### 3. Navigation And Discovery

- the app must support both file-system navigation and graph/wiki structure navigation
- opening a resource must update the editor tab and linked context surfaces
- orphaned or missing targets must be visible

### 4. Degraded Truth And Diagnostics

- `offline`, `mcp_disconnected`, `provider_unavailable`, `missing_scope`, and similar states must be shown explicitly
- degraded state must not block local authoring
- the app must provide recovery CTAs instead of silent fallback

### 5. Local Artifact Authority

The public product contract assumes these local artifacts remain authoritative:

- `.seojeom/project.json`
- `.seojeom/godot-workspace.json`
- `.seojeom/graph/canonical-slice.json`
- `.seojeom/graph/proposal-sets.json`
- `.seojeom/graph/local-pins.json`

## Acceptance Criteria

- a first-run user can create a project and enter the workbench immediately
- relaunch restores the last project and working context
- degraded AI or MCP state does not block project, file, or graph authoring
- local artifact ownership remains explicit and stable
