# Seojeom Desktop Authoring & Review PRD

## Purpose

This document defines the practical product contract for wiki authoring, episode authoring, graph authoring, review/apply flow, and in-app MCP operator visibility in Seojeom Desktop.

## Product Goal

Users should be able to write, structure, inspect, and approve changes inside one local-first workspace. External AI can assist, but review boundaries must remain visible and explicit.

## Scope

- wiki authoring
- episode and general file authoring
- graph authoring
- review queue and apply flow
- in-app MCP operator surface

## Core Requirements

### 1. Wiki Authoring

- wiki files follow local file authority
- root and subdocument ownership must remain visible
- graph-linked wiki open and create actions must exist
- external file conflicts must offer compare or reload paths instead of silent overwrite

### 2. Episode And General File Authoring

- episode and file editing must live inside the same shell
- autosave and explicit save both need to exist
- dirty-state guards must protect tab close and project switch
- review targets must reopen the correct file context

### 3. Graph Authoring

- users must be able to create, edit, and delete nodes and edges locally
- graph interaction must support direct manipulation, selection, and relation editing
- graph ownership links to wiki documents must be manageable from the graph surface
- saved camera state, local pins, and similar workspace context must persist locally

### 4. Review Queue And Apply

- proposal sets must remain separate from canonical graph data
- queue summary and diff inspection have different responsibilities
- approve, reject, and apply must be distinct actions
- canonical graph state must not change before apply

### 5. MCP Operator Surface In App

- the app must expose sidecar start, stop, refresh, and readiness state
- pending approval or proposal state must be visible in-app
- MCP failure must not block local authoring

## Acceptance Criteria

- wiki, episode, and graph authoring work in one shell
- review and canonical state remain separate
- external AI assistance enters through reviewable surfaces
- MCP state remains visible from inside the desktop app
