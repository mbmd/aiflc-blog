---
title: "Run Your First Project Initiation in 10 Minutes with AI-PILC"
date: 2026-07-06
author: "Mohammad Maheri"
categories: [tutorials]
tags: [quickstart, ai-pilc, walkthrough, initiation]
description: "Go from a one-line project idea to a complete Project Initiation Package in 10 minutes — structured, governed, and ready for architecture."
image: /assets/images/first-pilc-run-hero.png
difficulty: beginner
time_to_complete: "10 minutes"
---

## What You'll Build

By the end of this tutorial, you'll have a complete Project Initiation Package (PIP) — the structured foundation every project needs before architecture and coding begin. It includes a project charter, stakeholder register, feasibility assessment, risk register, and scope statement. All produced by your AI agent, governed by gates you approve.

```
your-project/
└── .aiflc/pdlc/ai-pilc-output/
    ├── 01-project-charter/
    ├── 02-scope-statement/
    ├── 03-feasibility-assessment/
    ├── 04-stakeholder-register/
    ├── 05-risk-register/
    ├── 06-resource-plan/
    ├── 07-communication-plan/
    ├── 08-quality-plan/
    ├── 09-success-criteria/
    └── 10-project-brief/
```

## Prerequisites

- An AI-enabled IDE (Kiro, Cursor, Claude Code, or VS Code with Copilot)
- Git installed
- 10 minutes
- A project idea (even a one-liner is enough)

## Step 1: Clone the AIFLC Repository

```bash
git clone https://github.com/mbmd/AIPDLC.git
```

You now have the full AI-* PDLC Family locally. We'll focus on AI-PILC.

## Step 2: Install AI-PILC Into Your Project Workspace

Open your existing project (or create a new empty folder). Follow the install guide for your IDE:

```bash
# For Kiro users:
# Copy the AI-PILC steering files to your project
# See INSTALL_GUIDE_KIRO.md in the repo root for exact paths
```

The installer places AI-PILC's workflow rules into your workspace's steering directory. Your AI agent can now see and follow the initiation lifecycle.

## Step 3: Start the Initiation Workflow

Open your AI chat and provide your project requirement. It can be as simple as:

```
I want to build a customer feedback portal that integrates with our 
existing Slack workspace and allows team leads to tag, prioritize, 
and respond to feedback items.
```

AI-PILC's workflow activates automatically. Your agent will begin Stage 1 (Project Charter) — asking clarifying questions, drafting the charter, and presenting it for your approval.

## Step 4: Approve Gates as You Go

At each stage boundary, the agent pauses and presents its output for your review. You'll see something like:

```
── GATE: Stage 1 → Stage 2 ─────────────────────────
I've drafted the Project Charter. Here's what it contains:
- Project name, sponsor, objectives
- High-level scope boundaries
- Key constraints and assumptions
- Success criteria (measurable)

Please review and approve to proceed to Scope Statement, 
or provide feedback for revision.
────────────────────────────────────────────────────────
```

Review the output. If it looks good, approve. If something's off, tell the agent what to adjust. The gate won't progress without your sign-off.

## Step 5: Complete All Stages

Continue through the remaining stages. Each builds on the previous:

| Stage | Produces | Takes ~|
|-------|----------|--------|
| 1. Project Charter | Objectives, scope, sponsor | 2 min |
| 2. Scope Statement | Boundaries, exclusions, deliverables | 1 min |
| 3. Feasibility Assessment | Technical, operational, financial viability | 2 min |
| 4. Stakeholder Register | Who's involved, their influence, needs | 1 min |
| 5. Risk Register | Top risks, probability, impact, response | 1 min |
| 6. Resource Plan | People, tools, budget estimate | 1 min |
| 7. Communication Plan | Who gets told what, when, how | 1 min |
| 8. Quality Plan | Acceptance criteria, review process | 1 min |
| 9. Success Criteria | Measurable outcomes tied to objectives | 0.5 min |
| 10. Project Brief | Executive summary of the full PIP | 0.5 min |

Total: ~10 minutes of wall-clock time for a complete Project Initiation Package.

## What You've Built

You now have a structured, auditable initiation package sitting in your project repository. This isn't throwaway documentation — it's the contracted input for the next packages in the chain:

- **AI-POLC** reads the PIP to produce a Product Backlog Package
- **AI-UXD** reads the PIP + PBP to design user experiences
- **AI-ADLC** reads all upstream outputs to design architecture
- **AI-DWG** consumes everything to generate your development workspace

Every decision you made in initiation — scope boundaries, risk acceptance, quality criteria — will flow forward and influence architecture, governance, and workspace structure. Nothing gets lost. Nothing gets re-asked.

## Troubleshooting

| Issue | Fix |
|-------|-----|
| Agent doesn't follow PILC stages | Ensure steering files are installed in the correct path. Check your IDE's steering/rules documentation. |
| Agent skips gates | Remind it: "Follow the AI-PILC workflow — do not progress without my gate approval." |
| Output feels generic | Provide more specific inputs. The richer your initial requirement description, the more tailored the PIP. |

## Next Steps

- **Go deeper:** Run AI-POLC next to produce a Product Backlog from your PIP
- **Try architecture:** Jump to AI-ADLC to see how your initiation decisions shape architecture
- **Explore the chain:** Read the [FAMILY_STRUCTURE.md](https://github.com/mbmd/AIPDLC) to understand how all 11 packages connect

---

*Part of the [AIFLC Tutorials series](https://blog.aiflc.dev/tutorials/). Questions? Open a [GitHub Discussion](https://github.com/mbmd/AIPDLC/discussions).*
