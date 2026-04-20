# CI/CD Testing: Add E2E Tests to Your Deployment Pipeline

Companion code for the Autonoma blog post 'CI/CD Testing: Add E2E Tests to Your Deployment Pipeline'.

> Companion code for the Autonoma blog post: **[CI/CD Testing: Add E2E Tests to Your Deployment Pipeline](https://getautonoma.com/blog/ci-cd-testing)**

## Requirements

Node 18+. Playwright 1.44+ (where applicable). An account and API token with Autonoma (for the Autonoma examples). A deployment platform that emits preview URLs (Vercel, Netlify, GitLab Review Apps, or equivalent).

## Quickstart

```bash
git clone https://github.com/Autonoma-Tools/ci-cd-testing.git
cd ci-cd-testing
# Copy the YAML file for your CI provider into your repo at the suggested path,
# set the required secrets (AUTONOMA_TOKEN for the Autonoma examples; your
# deployment platform's preview URL is extracted from the event payload or
# Review App URL), and push. Playwright examples assume Node 18+ and a
# playwright.config.ts in the repo root.
```

## Project structure

```
.
├── .circleci/
│   └── config.yml                  # CircleCI Playwright pipeline
├── .github/
│   └── workflows/
│       ├── autonoma.yml            # GitHub Actions + Autonoma (short path)
│       └── e2e.yml                 # GitHub Actions + Playwright (raw path)
├── .gitlab-ci.yml                  # GitLab CI + Playwright (raw path)
├── .gitlab-ci-autonoma.yml         # GitLab CI + Autonoma via cURL
├── bitbucket-pipelines.yml         # Bitbucket Pipelines + Playwright
├── LICENSE
├── package.json                    # Shared npm deps for the Playwright examples
└── README.md
```

- `src/` — primary source files for the snippets referenced in the blog post.
- `examples/` — runnable examples you can execute as-is.
- `docs/` — extended notes, diagrams, or supporting material (when present).

## About

This repository is maintained by [Autonoma](https://getautonoma.com) as reference material for the linked blog post. Autonoma builds autonomous AI agents that plan, execute, and maintain end-to-end tests directly from your codebase.

If something here is wrong, out of date, or unclear, please [open an issue](https://github.com/Autonoma-Tools/ci-cd-testing/issues/new).

## License

Released under the [MIT License](./LICENSE) © 2026 Autonoma Labs.
