# GitHub Info

## Mona's editorial angle

Mona's website focuses on practical GitHub guidance backed by official references from:

- docs.github.com
- github.blog
- github.blog/changelog

## Current homepage themes

- GitHub collaboration basics: repositories, branches, pull requests, and merges.
- GitHub Copilot as an AI coding assistant across the IDE, CLI, and GitHub.
- GitHub Actions as the automation layer behind repository workflows.
- Recent GitHub Blog and Changelog stories worth watching.

## Recent updates worth watching

- **Copilot code review can now approve pull requests.** Copilot's automated review can approve PRs directly, not just leave comments — useful for teams that want to speed up low-risk merges. (Source: GitHub Changelog, github.blog/changelog)
- **Configure cost vs. quality in Copilot's auto model selection.** Admins can now tune how Copilot balances cost and quality when it automatically picks a model for a task. (Source: GitHub Changelog, github.blog/changelog)
- **Refreshed repository pull requests page (public preview).** A redesigned PR list view is rolling out — worth trying if you manage many open PRs. (Source: GitHub Changelog, github.blog/changelog)
- **Control GitHub Actions cache access with `cache-mode`.** New setting lets you restrict which workflows can read/write the Actions cache, reducing supply-chain risk. (Source: GitHub Changelog, github.blog/changelog)
- **Block pull requests with exposed secrets from merging.** Secret scanning can now stop a PR from merging if it contains a detected secret. (Source: GitHub Changelog, github.blog/changelog)
- **"GitHub Copilot app for Beginners" series.** New beginner tutorials cover using diff/terminal/browser views and running multiple Copilot agents in parallel — a good starting point for readers new to Copilot's agent mode. (Source: GitHub Blog, github.blog/latest)
- **How GitHub makes AI coding more cost efficient.** A blog post explains how Copilot reduces wasted compute across an entire coding task rather than just shortening individual responses. (Source: GitHub Blog, github.blog/latest)

## Agentic workflows: Awesome Copilot workflows directory

The [Awesome Copilot workflows directory](https://awesome-copilot.github.com/workflows/) is a community-maintained catalog of ready-to-use, scheduled Copilot-agent workflows (GitHub Actions jobs) that teams can drop into a repo, including:

- Daily/weekly issue and PR digests (e.g., `daily-issues-report`, `ospo-org-health`)
- Contributor activity and release-compliance reports (`ospo-contributors-report`, `ospo-release-compliance-checker`)
- Stale repository and content-relevance checks (`ospo-stale-repos`, `relevance-check`)

Each workflow is a Markdown file with YAML frontmatter (trigger, permissions, `safe-outputs`, engine) plus a natural-language prompt — a practical starting point for readers who want automation patterns without building one from scratch.
