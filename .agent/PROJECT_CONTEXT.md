# Project Context — GitHub Profile README

## Overview

| Field | Value |
|-------|-------|
| **Repository** | `doctor500/doctor500` (special profile repo) |
| **Purpose** | GitHub profile landing page |
| **Branch** | `master` |
| **Main File** | `README.md` (root) |
| **Owner** | David Layardi |
| **Created** | 2026-02-15 |

## Architecture

The `README.md` in a user-named repo (`doctor500/doctor500`) is a GitHub special repository — its content appears on the user's profile page at [github.com/doctor500](https://github.com/doctor500).

### File Structure

```
doctor500/
├── .agent/
│   ├── PROJECT_CONTEXT.md    # This file
│   └── README.md             # Agent directory overview
├── .github/
│   └── workflows/
│       └── snake.yml         # Daily contribution snake SVG generator
└── README.md                 # Profile README (main content)
```

## README Sections

The `README.md` contains these sections in order:

| # | Section | Description | External Dependencies |
|---|---------|-------------|-----------------------|
| 1 | **Hero (Typing SVG)** | Animated cycling text | `readme-typing-svg.demolab.com` |
| 2 | **Social Badges** | Profile Views, LinkedIn, Medium, Website, Email | `komarev.com`, `shields.io` |
| 3 | **About Me** | Short bio with emoji bullets | None (static markdown) |
| 4 | **Tech Stack** | Shields.io badges grouped by 7 categories | `shields.io` |
| 5 | **GitHub Stats** | Stats card, Top Languages, Streak | `github-readme-stats.vercel.app`, `github-readme-streak-stats.herokuapp.com` |
| 6 | **Featured Projects** | 4 pinned repo cards | `github-readme-stats.vercel.app` |
| 7 | **Contribution Snake** | Animated SVG snake eating contribution graph | Self-hosted via GitHub Action (`output` branch) |
| 8 | **Let's Connect** | CTA with LinkedIn badge | `shields.io` |

## External Services & Dependencies

### Typing SVG
- **Service:** [readme-typing-svg.demolab.com](https://readme-typing-svg.demolab.com)
- **Config:** `font=Fira+Code`, `size=24`, `width=460`, `color=#70A5FD`
- **Lines (URL-encoded):**
  - `Cloud • DevOps • Agentic AI`
  - `Kubernetes • Terraform • CI/CD`
  - `AI-Driven Infrastructure Ops 🚀`
  - `Based in Tokyo, Japan 🗼`
- **⚠️ Width constraint:** GitHub's README container is ~680px. Keep all lines under ~30 characters at size=24 to avoid truncation.

### Shields.io Badges
- **Service:** [shields.io](https://shields.io)
- **Style:** `for-the-badge`
- **Icons:** [Simple Icons](https://simpleicons.org)
- **Used for:** Social links, tech stack, CTA button

### GitHub Readme Stats
- **Service:** [github-readme-stats.vercel.app](https://github.com/anuraghazra/github-readme-stats)
- **Theme:** `tokyonight` with custom colors
- **Cards used:** Stats, Top Languages, Repo Pins
- **Custom colors:** `bg_color=0D1117`, `title_color=70A5FD`, `icon_color=70A5FD`, `text_color=FFFFFF`
- **⚠️ Rate limits:** Vercel-hosted — may show broken images during high traffic. Self-hosting is the permanent fix.

### GitHub Streak Stats
- **Service:** [github-readme-streak-stats.herokuapp.com](https://github.com/DenverCoder1/github-readme-streak-stats)
- **Theme:** `tokyonight` with custom overrides
- **Custom:** `fire=FF6B6B`, `ring=70A5FD`

### Profile Views Counter
- **Service:** [komarev.com/ghpvc](https://github.com/antonkomarev/github-profile-views-counter)
- **Style:** `for-the-badge`, `color=70a5fd`

### Contribution Snake
- **GitHub Action:** `.github/workflows/snake.yml`
- **Uses:** `Platane/snk@v3`
- **Schedule:** Daily at 00:00 UTC
- **Output:** Pushes `github-snake-dark.svg` to `output` branch
- **Referenced as:** `https://raw.githubusercontent.com/doctor500/doctor500/output/github-snake-dark.svg`
- **⚠️ First run:** Must be triggered manually after merge (Actions → Generate Snake → Run workflow)

## Design System

| Token | Value | Usage |
|-------|-------|-------|
| Primary color | `#70A5FD` | Titles, badges, accents |
| Background | `#0D1117` | Stats card backgrounds |
| Text | `#FFFFFF` | Stats card text |
| Fire/streak | `#FF6B6B` | Streak fire accent |
| Font | Fira Code | Typing SVG header |
| Badge style | `for-the-badge` | All shields.io badges |
| Stats theme | `tokyonight` | All github-readme-stats cards |

## Tech Stack Categories

Badges are organized into these groups (update `README.md` when skills change):

1. **Cloud Platforms** — AWS, GCP
2. **Container & Orchestration** — Docker, Kubernetes, Helm
3. **CI/CD & Automation** — Jenkins, GitHub Actions, ArgoCD, GitLab CI
4. **Infrastructure as Code** — Terraform
5. **AI & Agentic Tools** — Claude Code, MCP Protocol
6. **Languages & Scripting** — Python, Go, Bash, Groovy
7. **Monitoring & Observability** — Datadog, Prometheus, Grafana, New Relic

## Featured Repositories

Currently pinned repos (update when new showcase repos are available):

| Repo | Description |
|------|-------------|
| `cv` | Markdown CV → PDF pipeline with GitHub Actions |
| `landing-page` | Static landing page with AI-ready integration |
| `ubuntu-ai` | AI-assisted Ubuntu VM management |
| `publication-blog` | Static blog powered by Outstatic CMS |

## Maintenance Guide

### When to update README.md:
- New job role or company change → Update About Me section
- New skills acquired → Add badges to Tech Stack
- New notable project → Add/replace in Featured Projects
- Profile positioning change → Update Typing SVG lines

### When to update this context:
- New external services added
- Design tokens changed
- Section structure modified
- New GitHub Actions added

## Troubleshooting

| Issue | Cause | Fix |
|-------|-------|-----|
| Stats cards show broken image | Vercel rate limit | Wait 1-2 hours, or self-host |
| Snake SVG missing | `output` branch not created | Manually trigger snake workflow |
| Typing SVG truncated | Text too long for width | Shorten lines or reduce `size` param |
| Badges not rendering | shields.io outage | Check [status.shields.io](https://status.shields.io) |
| Profile Views stuck at 0 | Counter initializing | Views increment on unique visits |

---

*Last updated: 2026-02-15*
