# AIFLC Blog

Engineering, methodology, and product insights from the AI-* Family lifecycle system.

## Tech Stack

- **Generator:** Hugo (Extended)
- **Theme:** PaperMod
- **Hosting:** GitHub Pages
- **Deployment:** GitHub Actions (auto-deploy on push to main)

## Local Development

`ash
hugo server -D
`

Open http://localhost:1313 to preview (including drafts).

## Publishing

Push to main branch. GitHub Actions builds and deploys automatically.

## Content Structure

`
content/
  engineering/    - How AIFLC works (deep dives)
  product/        - Package launches, features, roadmap
  methodology/    - Thought leadership, process philosophy
  open-source/    - Community, licensing, contributions
  tutorials/      - Step-by-step guides
  changelog/      - Per-release notes
`

## Adding a Post

`ash
hugo new content content/methodology/my-new-post.md
`

Edit the file, set draft: false when ready, push.

## Links

- **Live site:** https://mbmd.github.io/aiflc-blog/
- **AIFLC (brand hub):** https://github.com/mbmd/AIFLC
- **AI-* PDLC Family (packages):** https://github.com/mbmd/AIPDLC
