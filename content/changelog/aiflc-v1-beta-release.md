---
title: "AI-* PDLC Family v1.0-beta — First Public Release"
date: 2026-07-06
author: "Mohammad Maheri"
categories: [changelog]
tags: [release, v1.0-beta, pdlc, all-packages]
description: "Release notes for the AI-* PDLC Family v1.0-beta — 11 packages, full lifecycle chain, Apache 2.0."
---

## Summary

The first public beta of the AI-* PDLC Family is available. All 11 packages are complete, tested, and chaining correctly. Drop them into any AI-enabled IDE workspace.

## Changes

### Added

- **AI-ILC** — Idea Lifecycle: raw idea → validated Idea Brief (optional pre-stage)
- **AI-PILC** — Project Initiation Lifecycle: requirement → Project Initiation Package (10 stages, gated)
- **AI-PPM** — Portfolio Management: multi-project prioritization and governance engine
- **AI-FLO** — Flow Orchestrator: package-to-package routing across layers
- **AI-POLC** — Product Ownership Lifecycle: PIP → Product Backlog Package
- **AI-UXD** — UX Design Lifecycle: PIP + PBP → UX Design Package (personas, flows, tokens, accessibility)
- **AI-ADLC** — Architecture Design Lifecycle: PIP + PBP + UXP → Architecture Package (ADRs, C4, NFRs)
- **AI-DWG** — Workspace Generator: AP + PBP + UXP → ready-to-code development workspace
- **AI-GCE** — Governance & Compliance Engine: architecture → enforceable workspace rules
- **AI-TGE** — Test Governance Engine: continuous quality alongside build lifecycle
- **Chain contracts** — every package declares typed inputs/outputs; downstream consumes upstream automatically
- **Multi-IDE support** — install guides for Kiro, Cursor, Claude Code, Copilot, Cline, Amazon Q, Codex, VS Code
- **Family documentation** — FAMILY_STRUCTURE, FAMILY_INTERFACE, gate protocols, contributing guide

### Architecture Decisions

- Sequential project-layer flow (POLC→UXD→ADLC→DWG) with defined feedback loops
- Portfolio layer operates across projects; project layer scopes to one
- AI-FLO sits on the edge between layers as the router
- AI-GCE and AI-TGE run alongside AI-DLC v1 (not sequentially)
- File-based contracts (markdown) — no API dependencies, works offline

### Licensing

- Apache 2.0 for all packages
- CLA required for contributions (to protect commercial services layer)
- Full licensing FAQ included

## Migration Notes

This is the first release — no migration needed. Fresh install only.

## Links

- [GitHub Repository](https://github.com/mbmd/AIPDLC)
- Install Guides:
  - [Kiro](https://github.com/mbmd/AIPDLC/blob/main/INSTALL_GUIDE_KIRO.md)
  - [Claude Code](https://github.com/mbmd/AIPDLC/blob/main/INSTALL_GUIDE_CLAUDE.md)
  - [Codex](https://github.com/mbmd/AIPDLC/blob/main/INSTALL_GUIDE_CODEX.md)
  - [Cursor](https://github.com/mbmd/AIPDLC/blob/main/INSTALL_GUIDE_CURSOR.md)
  - [GitHub Copilot](https://github.com/mbmd/AIPDLC/blob/main/INSTALL_GUIDE_COPILOT.md)
  - [Cline](https://github.com/mbmd/AIPDLC/blob/main/INSTALL_GUIDE_CLINE.md)
  - [Amazon Q](https://github.com/mbmd/AIPDLC/blob/main/INSTALL_GUIDE_AMAZONQ.md)
  - [VS Code (generic)](https://github.com/mbmd/AIPDLC/blob/main/INSTALL_GUIDE_VSCODE.md)
- [Contributing](https://github.com/mbmd/AIPDLC/blob/main/CONTRIBUTING.md)
- [Report an issue](https://github.com/mbmd/AIPDLC/issues)
