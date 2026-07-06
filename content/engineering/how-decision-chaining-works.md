---
title: "How Decision-Chaining Actually Works Inside AIFLC"
date: 2026-07-06
author: "Mohammad Maheri"
categories: [engineering]
tags: [chain, contracts, architecture, lifecycle]
description: "A technical deep dive on how AIFLC packages pass contracted outputs forward — so decisions made in initiation become enforceable rules in code."
image: /assets/images/decision-chaining-hero.png
---

Most lifecycle tools stop at documentation. You write an architecture decision, it lives in a wiki, and two months later nobody enforces it. The AIFLC chain works differently — every package produces a contracted output that becomes the contracted input for the next package downstream.

This post explains the mechanics.

## The Problem We Faced

AI coding agents are fast at executing. They're terrible at remembering context across phases. Ask an agent to build a workspace today based on architecture decisions you made last week, and you'll find yourself re-explaining everything. The context is gone.

Traditional tools don't help because they store decisions in places the agent never sees — Confluence pages, Jira tickets, Notion docs. The decisions exist, but they're not *available* at the point of execution.

We needed a way to make upstream decisions physically present when downstream execution happens — without requiring the user to copy-paste or re-explain.

## Why This Is Harder Than It Looks

The naive solution is "just pass the files forward." But that breaks immediately for three reasons:

1. **Shape mismatch.** A project initiation package has different structure than what an architecture workflow needs as input. You can't just hand a 200-page PIP to AI-ADLC and expect it to find the relevant bits.

2. **Selective consumption.** Each downstream package needs specific slices of the upstream output — not all of it. AI-DWG needs architecture decisions and backlog stories, but not the financial projections from initiation.

3. **Enforcement gap.** Passing information forward doesn't guarantee it's used. Without contracts, downstream packages can silently ignore upstream decisions.

## Our Approach: Typed Contracts at the Chain Boundary

Every package in the AI-* PDLC Family declares:
- **Input type** — exactly what it expects to receive
- **Output type** — exactly what it guarantees to produce

This creates a chain of contracts:

```
AI-ILC outputs:   Approved Idea Brief
AI-PILC outputs:  Project Initiation Package (PIP)
AI-POLC outputs:  Product Backlog Package (PBP)
AI-UXD outputs:   UX Design Package (UXP)
AI-ADLC outputs:  Architecture Package (AP)
AI-DWG consumes:  AP + PBP + UXP → Ready-to-code Development Workspace (DW)
```

Each output is a structured set of markdown files with defined sections. Not a loose folder — a typed deliverable with known structure that the next package's workflow can locate and consume programmatically.

## How It Works in Practice

When AI-ADLC finishes its architecture workflow, it produces an Architecture Package with defined artifacts: ADRs, C4 diagrams, technology selections, NFR specifications. These files land in a known location with a known structure.

When AI-DWG starts, its generator reads the AP directory and extracts exactly the sections it needs: which technologies were selected (to scaffold the correct toolchain), which ADRs were decided (to generate workspace hooks that enforce them), and which NFRs apply (to configure linting and quality gates).

The same is true upstream. AI-ADLC doesn't start from scratch — it reads the PIP from AI-PILC (for scope, constraints, and success criteria) and the PBP from AI-POLC (for feature boundaries and acceptance criteria). Architecture decisions are grounded in business requirements that were decided two packages ago.

```
User's workspace after running the chain:

project/
├── .aiflc/pdlc/                   ← Installed lifecycle home
│   ├── ai-pilc-output/            ← PIP (contracted)
│   │   ├── 01-project-charter/
│   │   ├── 04-stakeholder-register/
│   │   └── ...
│   ├── ai-polc-output/            ← PBP (contracted)
│   │   ├── product-backlog/
│   │   ├── user-stories/
│   │   └── ...
│   ├── ai-uxd-output/             ← UXP (contracted)
│   │   ├── personas/
│   │   ├── user-flows/
│   │   └── ...
│   └── ai-adlc-output/            ← AP (contracted)
│       ├── adrs/
│       ├── c4-model/
│       └── ...
├── .kiro/steering/                ← Rules generated from architecture
└── src/                           ← Code scaffold matching architecture
```

The development workspace wasn't configured by hand. It was *derived* from architecture decisions, which were derived from product scope, which was derived from the initiation charter. Each step is traceable backward through the chain.

## What We Learned

- **Contracts at boundaries matter more than flexibility.** The early temptation was to make everything optional and adaptive. That led to packages silently receiving empty inputs and producing incomplete outputs. Strict typing at the boundary — with explicit "subset mode" declarations for brownfield scenarios — works far better.

- **The chain is sequential, not parallel.** We tried parallel execution (POLC and ADLC at the same time) and it created merge conflicts in decisions. Sequential flow — POLC→UXD→ADLC→DWG — with defined feedback loops is simpler and produces better results.

- **File-based contracts are surprisingly robust.** We considered API-based orchestration, databases, event buses. Markdown files in known locations turned out to be the most portable, debuggable, and AI-readable format. Every agent can read a file. Not every agent can call an API.

## Try It Yourself

The full chain is [available on GitHub](https://github.com/mbmd/AIPDLC). Start with [AI-PILC](https://github.com/mbmd/AIPDLC) for project initiation — it produces the PIP that feeds every downstream package. Drop it into your workspace and experience how decisions flow forward without re-explanation.

---

*Mohammad Maheri is the creator of AIFLC — a free, open-source lifecycle system for AI coding agents. [GitHub](https://github.com/mbmd/AIPDLC) · [LinkedIn](https://linkedin.com/in/mbmd)*
