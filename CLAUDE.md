# Claude Context — Terraform Portfolio

## Project Purpose
Hands-on Terraform study and portfolio project. Built to demonstrate progressive Terraform skills across multiple providers — from basics to production-grade patterns. Doubles as exam prep for **Terraform Associate (004)**, which covers Terraform 1.12.

## Owner
Clayton Speak — senior technologist.  Azure is primary cloud depth, AWS is where we're starting because that's the current tutorial track.

## Repo Structure
```
terraform-portfolio/
├── CLAUDE.md
├── README.md
├── .gitignore
├── aws/                  # Active — building this first
│   ├── 01-basics/
│   ├── 02-variables/
│   ├── 03-outputs/
│   ├── 04-data-sources/
│   ├── 05-modules/
│   ├── 06-state-management/
│   └── 07-workspaces/
├── azure/                # Planned
├── gcp/                  # Planned
├── okta/                 # Planned
└── modules/              # Shared reusable modules
```

## Current State
- Repo structure created, not yet pushed to GitHub
- AWS section is active — working through 01-basics first
- Azure, GCP, Okta directories are placeholders

## Conventions
- Terraform >= 1.12
- Numbered directories show progression (01, 02, etc.)
- Each example directory should have its own README explaining what it covers
- `.tfvars` files are gitignored — use `.tfvars.example` for showing example values
- Keep examples self-contained and runnable

## Goals
- Each provider section builds from simple to complex
- Examples should be portfolio-quality: clean, commented, readable
- AWS first, then Azure (primary depth), then GCP and Okta
- No over-engineering — practical, real-world patterns only