---
title: "Why We Chose Apache 2.0 + Attribution for the PDLC Family (And What That Means for You)"
date: 2026-07-06
author: "Mohammad Maheri"
categories: [open-source]
tags: [apache-2.0, licensing, community, open-source, pdlc, attribution]
description: "The reasoning behind the AI-* PDLC Family's Apache 2.0 + Attribution license — and why it matters whether you're a solo developer, a consultant, or an enterprise."
image: /assets/images/apache-2-choice-hero.png
---

## The Decision Point

When you build something you intend to give away — genuinely give away, not "free tier with an upsell gate" — the license is the first real decision. It signals intent. It defines the relationship between creator and user. And it's very hard to change later.

We chose **Apache 2.0 with one Attribution Addendum** for the **AI-* PDLC Family** (the first published family within AIFLC). Not MIT. Not GPL. Not a custom "source-available" license. Here's why, and what it practically means for you.

**A note on scope:** AIFLC is a brand that contains multiple families. The PDLC family is the first — and its license is Apache 2.0 + Attribution. Future families may choose different licensing models depending on their audience and commercial context. This post explains the PDLC decision specifically.

## The Context

The AI-* PDLC Family is a lifecycle system — 11 workflow packages that guide AI coding agents through structured delivery. It's not a SaaS. It's not a library you `npm install`. It's markdown files and steering rules that live in your repository. Which means the license question is slightly unusual: you're not linking to our code at runtime. You're *using our structure* to guide your own work.

That distinction matters for license selection.

## Why Not MIT for PDLC?

MIT is maximally permissive. Anyone can do anything, as long as they keep the copyright notice. For a library, that's usually fine. For a system people will build commercial practices around — consultancies training teams on it, enterprises embedding it in their delivery frameworks — MIT leaves two gaps: patent protection and brand visibility.

**Patent protection.** Apache 2.0 includes an explicit patent grant. If we hold any patents that read on the implementation, you get a license to those patents automatically when you use the code. MIT doesn't give you that. For enterprise legal teams evaluating whether to adopt, the patent grant is often the difference between "approved" and "needs further review."

**Brand visibility.** Neither MIT nor plain Apache 2.0 requires anyone to *show* where the work came from. MIT only asks you to retain a copyright line in the source; plain Apache asks the same. Once a product is compiled, deployed, or taught in a course, that origin becomes invisible to the people actually using it. Since adoption is the whole strategy here, we needed the credit to travel with the work — so we added one condition on top of Apache 2.0. More on that below.

## Why Not GPL for PDLC?

GPL would require anyone who modifies the PDLC packages and distributes them to release their modifications under the same license. That's a valid philosophical position — but it conflicts with our goal for this family.

We *want* consultancies to customize the PDLC packages for their clients without publishing those customizations. We *want* enterprises to fork and adapt internally without copyleft obligations. We *want* the barrier to adoption to be zero. GPL's copyleft requirement would create friction for exactly the users we most want to reach.

## Why Not Source-Available for PDLC?

Some projects use custom licenses that look open but restrict commercial use, competing products, or managed-service offerings. We considered this briefly and rejected it for a simple reason: it violates the signal we're trying to send.

The PDLC family's business model is services — consulting, training, certification, enterprise adoption support. The *product* is genuinely free. If we license-gate the product, we're not a services company — we're a SaaS with extra steps. The Apache 2.0 choice is the proof that the PDLC packages are actually free. No asterisks.

## The One Condition for PDLC: Attribution

Apache 2.0 gives you everything — use, modify, distribute, sell, sublicense. We added exactly one condition on top of it: attribution. If you distribute a product, service, course, or deliverable that's substantially based on the PDLC family, include this notice somewhere a user can see it:

> *Built on AIFLC by Mohammad Maheri — [LinkedIn](https://www.linkedin.com/in/mohammad-maheri-8399565b)*

That's the whole ask. A few specifics worth knowing:

- **Where it goes:** at least one prominent, user-visible place — a README, product documentation, an "About" page, or an app footer. Not buried in a source file nobody opens. One prominent location per distributed product is enough.
- **Internal use is exempt.** If you're using the packages inside your own team and not shipping a product to others, the attribution requirement doesn't trigger. It's about *distribution*, not use.
- **It applies to commercial and non-commercial distribution alike.** A paid consulting deliverable carries the notice the same way a free open-source fork does.
- **It's not an endorsement.** Displaying the notice doesn't mean we endorse, certify, or sponsor your product. It's credit, nothing more.

This is the one place where the PDLC license goes beyond stock Apache 2.0. We were deliberate about it: the whole model depends on the work being *visible* as it spreads. Dropping the attribution notice is the only thing that puts you in breach — and even then there's a 30-day cure window for a first slip.

## What the PDLC License Means for You

**If you're a solo developer:** Use the PDLC packages however you want. Commercially, personally, experimentally. Modify them. Share them. The obligations are minimal: keep the LICENSE and NOTICE files intact, and — if you distribute something built on them — include the attribution notice above.

**If you're a consultancy or system integrator:** Build client delivery frameworks on top of the PDLC family. Customize packages for your methodology. Train your team. Sell the expertise. You don't owe us royalties or revenue share. The one thing you do owe is the attribution notice — visible in the deliverables, courses, or products you ship to clients. That's it. This is by design — we want you building on this.

**If you're an enterprise:** Your legal team can approve Apache 2.0 on day one. No procurement cycle. No vendor risk assessment (we're not a vendor — we're an open-source project). The patent grant covers you. Fork it, run it internally, modify it to match your governance framework. If we disappear tomorrow, the code is still yours.

**If you want to contribute:** We use a Contributor License Agreement (CLA). This protects the ability to maintain the project and offer commercial services without contributor code creating licensing conflicts. The CLA doesn't transfer your copyright — you keep ownership of your contribution. It grants us a license to distribute your contribution under Apache 2.0 + Attribution, or any future license the project adopts. Standard practice for projects with dual open-source/services models.

## The Bet We're Making for PDLC

Apache 2.0 for the PDLC family is a bet that giving the product away completely — no gates, no tiers, no "enterprise edition" — builds a community large enough that services demand follows naturally. It's the Red Hat model, the Elastic model (before the license change), the Hashicorp model (before the license change).

The difference that matters for you: **every version we release under Apache 2.0 stays that way forever.** Open-source licenses can't be revoked for versions already published — once a release is out under Apache 2.0 + Attribution, that grant is irrevocable for everyone who received it. So there's no "rug pull" risk on what's already shipped. If we ever changed terms for a *future* version, the code you already have remains free under the license it came with. Fork it and you're covered permanently.

Future families within AIFLC will make their own licensing decisions based on their audience, commercial model, and distribution strategy. Apache 2.0 + Attribution is not a blanket commitment across the entire brand — it's a deliberate choice for the PDLC family, and the versions released under it are permanent.

## Get Involved

- **Use it:** [GitHub Repository](https://github.com/mbmd/AIPDLC) — clone, install, run
- **Extend it:** [Contributing Guide](https://github.com/mbmd/AIPDLC/blob/main/CONTRIBUTING.md) — CLA sign-off, then PR
- **Fork it:** Your right under Apache 2.0. Build something new on top (keep the attribution notice). We'd love to hear about it.
- **Tell people:** If the PDLC family helped your team, share it. Word of mouth is how open-source grows.

---

*The AI-* PDLC Family is Apache 2.0 + Attribution — free to use, modify, and build upon, with credit to the original work. [GitHub](https://github.com/mbmd/AIPDLC) · [Contributing Guide](https://github.com/mbmd/AIPDLC/blob/main/CONTRIBUTING.md)*
