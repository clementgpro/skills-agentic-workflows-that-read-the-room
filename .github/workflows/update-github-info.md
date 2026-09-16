---
name: update-github-info
description: Keep the GitHub Info content current with official GitHub Blog and Changelog updates.
on:
  schedule: daily
  workflow_dispatch:
permissions:
  contents: read
  pull-requests: read
engine: copilot
tools:
  github:
    toolsets: [repos]
  web-fetch:
  edit:
network:
  allowed:
    - github.blog
    - github.com
safe-outputs:
  create-pull-request:
    max: 1
    draft: true
---

# Update GitHub Info

Keep Mona's GitHub Info website current while preserving her editorial direction.

## Required reading

1. Read `notes/mona-notes.md` before making any change.
2. Use the GitHub repository API tools to read repository guidance and reference files. Do not use terminal, CLI, or sandboxed shell commands for repository guidance or reference-file reading.
3. Use `web-fetch` to read both public official sources:
   - `https://github.blog/latest/`
   - `https://github.blog/changelog/`

## Update rules

- Select only concise, practical updates that help developers learn GitHub faster.
- Prefer official GitHub Blog or Changelog items that fit the existing themes in `site/content/github-info.md`.
- Mention the source for every update, including the relevant official URL.
- Edit only `site/content/github-info.md`.
- Keep the existing Markdown structure and make the smallest useful content update.
- Do not invent facts, dates, links, or product details. If there is no worthwhile update, leave the file unchanged.

## Review handoff

After updating the content, inspect the diff and request exactly one `create-pull-request` safe output. The pull request must:

- target the repository's default branch;
- explain what changed and list the official source URLs;
- state that the change is ready for Mona to review;
- include only the intended update to `site/content/github-info.md`.

Do not write directly to the default branch, merge anything, or create any other output.