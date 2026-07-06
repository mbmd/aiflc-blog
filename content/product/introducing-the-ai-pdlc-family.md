---
title: "Introducing the AI-* PDLC Family — 11 Packages, One Connected Chain"
date: 2026-07-06
author: "Mohammad Maheri"
categories: [product]
tags: [release, family, pdlc, lifecycle, launch]
description: "The AI-* PDLC Family ships 11 packages that chain from raw idea to governed code — all free, file-based, and IDE-native."
image: /assets/images/pdlc-family-launch-hero.png
---

## What's New

Today, the AI-* PDLC (Product Development Life Cycle) Family is publicly available — 11 packages that guide your AI coding agent through every delivery phase, from the first rough idea to a fully governed, ready-to-code workspace. Each package produces contracted outputs that feed the next. No gaps. No re-explanation. One connected chain.

## Why We Built This

AI coding agents are remarkable at execution. Hand them a clear spec and they'll produce working code in minutes. But "clear spec" hides an enormous amount of upstream work — the initiation, the architecture, the governance, the portfolio decisions — that nobody was structuring.

The result: developers skip straight to code, accumulate design debt they can't see, and produce software that works today but can't evolve tomorrow. The problem isn't the agent. It's the absence of lifecycle around the agent.

We built the AI-* PDLC Family to fill that gap. Not a SaaS platform. Not a subscription. Just injectable markdown workflow packages that live in your repo and make your AI agent do the thinking work before the typing work.

## How It Works

The family is organized into two layers:

**Portfolio Layer** (scope = many projects):
- **AI-ILC** — Idea capture and validation. Turns a raw idea into an Approved Idea Brief.
- **AI-PILC** — Project initiation. Produces a full Project Initiation Package.
- **AI-PPM** — Portfolio governance. Manages prioritization across multiple projects.

**Edge Router:**
- **AI-FLO** — Orchestrates handoffs between packages and layers.

**Project Layer** (scope = one project):
- **AI-POLC** — Product ownership. Produces a Product Backlog Package.
- **AI-UXD** — UX design. Produces personas, user flows, IA, design tokens.
- **AI-ADLC** — Architecture. Produces ADRs, C4 models, technology selections.
- **AI-DWG** — Workspace generation. Produces a ready-to-code development workspace.
- **AI-GCE** — Governance engine. Enforces architecture decisions as workspace rules.
- **AI-TGE** — Test governance. Ensures quality through the build lifecycle.

All of these chain into **AI-DLC v1** (Amazon's open-source build lifecycle) — the existing tool that writes the code. We don't replace your coding agent. We give it the structured inputs it needs to produce better results.

## Key Principles

**Human-governed.** Every package has gates. Every gate requires human approval before the AI progresses. Your agent structures; you decide.

**File-based.** Everything is markdown. Lives in your repo. Works offline. No vendor lock-in. Move it anywhere.

**Free.** Apache 2.0. Use commercially, fork it, extend it. One condition: credit the author.

**Progressive.** Start with one package. See value immediately. Expand when you're ready. No big-bang rollout.

## What's Next

- Hugo-based blog with tutorials and deep dives (this one)
- GitHub Issues and Discussions for feedback and questions
- Per-package video walkthroughs
- Enterprise adoption guides

## Get Started

```bash
git clone https://github.com/mbmd/AIPDLC.git
```

Pick any package. Read its `README.md`. Follow the install guide. Your AI agent becomes a structured lifecycle partner in under 5 minutes.

→ [GitHub Repository](https://github.com/mbmd/AIPDLC)
→ [Install Guide](https://github.com/mbmd/AIPDLC/blob/main/INSTALL_GUIDE_KIRO.md)

---

*Released as part of AIFLC v1.0-beta. [Full repository](https://github.com/mbmd/AIPDLC) · [Contributing](https://github.com/mbmd/AIPDLC/blob/main/CONTRIBUTING.md)*
