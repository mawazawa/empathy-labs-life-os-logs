# EmpathyLabs Super-Repo

## Purpose

Super-repo for EmpathyLabs projects: ACDC, LilScrappy, Unigami, PrinciplesOS, LifeOS.

## Navigational Sitemap (4 levels deep, no node_modules)

```
EmpathyLabs/
├── .life-os/                          # LifeOS: Personal Operating System
│   └── PERSONAL_CONSTITUTION.md       # Presidential productivity framework
├── life-os-logs/                      # LifeOS: Conversation tracking
│   ├── conversation-log.md            # Verbatim conversation logs
│   └── README.md
├── LifeOS/                            # LifeOS: Personal productivity systems
│   ├── implementation-plan.md          # Voice notes automation phases
│   ├── linear-reorganization.md        # Team structure documentation
│   ├── README.md
│   └── team-consolidation-decision.md  # Single team decision rationale
├── PrinciplesOS/                      # PrinciplesOS: Operations & morals department
│   ├── decision-log.md                 # Decision tracking with review cadence
│   ├── decision-logging-sop.md         # SOP for decision logging
│   └── README.md
├── WorkOS/                             # WorkOS: Professional execution domain
│   ├── JusticeOS/                      # JusticeOS: Legal tech for the 99%
│   │   ├── components/                  # React components
│   │   ├── docs/                       # Documentation
│   │   ├── lib/                        # Core libraries
│   │   ├── migrations/                 # Database schema (90+ files)
│   │   ├── supabase/                   # Backend services
│   │   └── ui/                         # Frontend application
│   ├── BillHero/                       # WorkOS: Attorney billing automation
│   └── [Other professional projects]
├── ACDC/                               # PrinciplesOS: Autocatalytic Processes
│   └── README.md
├── LilScrappy/                        # WorkOS: Lightweight scraping toolkit
│   └── README.md
├── Unigami/                            # WorkOS: Unified gaming platform
│   └── README.md
├── package.json                        # pnpm workspace configuration
├── pnpm-workspace.yaml                 # Workspace definitions
└── README.md                           # This file
```

## Structure

- `ACDC/` — Continuous Learning Experiment & JackAss Award Tracking
- `LilScrappy/` — Lightweight scraping toolkit
- `Unigami/` — Unified gaming platform
- `PrinciplesOS/` — Operating principles and governance framework
- `LifeOS/` — Life management system

## Workspace

This repo uses **pnpm workspaces** for shared scripts and dependency efficiency.

```bash
# Install all dependencies across workspaces
pnpm install

# Run shared scripts
pnpm run lint
pnpm run format
pnpm run typecheck
```

## Hybrid Repo Model

We use a phased evaluation model for external tools:

### Phase 1: Evaluation (Subtree)
- Add external repo as a subtree to test and adjust locally.
- Remote stays external; we can pull updates.

### Phase 2: Internship (Subtree with adjustments)
- Continue using subtree; we may make local modifications.
- Sync upstream periodically via `git subtree pull`.

### Phase 3: Full-time (Submodule)
- Convert subtree to submodule to pin to a specific commit.
- Project becomes its own “baby” with its own remote.

#### Migration: Subtree → Submodule
```bash
# Remove subtree folder from index
git rm -r <folder>
git commit -m "remove <folder> subtree"

# Add as submodule
git submodule add <remote-url> <folder>
git commit -m "add <folder> as submodule"
```

## Onboarding

- Clone with `git clone https://github.com/mawazawa/empathy-labs.git && cd empathy-labs`
- Run `pnpm install` to bootstrap workspace dependencies.
- Each project folder contains its own README and development instructions.

## Notes

- JusticeOS lives in its own repo (https://github.com/mawazawa/JusticeOS) and is **not** included here to avoid dual-source-of-truth and secret-scanning issues.
- Submodule usage is reserved for third-party libs we want pinned; internal projects use subtree until they graduate to submodule.
