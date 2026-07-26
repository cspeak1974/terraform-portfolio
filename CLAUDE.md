# CLAUDE.md

Context file for Claude Code working in this repo.

## Purpose

Portfolio + study repo for the **Terraform Associate (004)** certification.
Each numbered directory under `aws/` maps to a section of HashiCorp's
official learning path:
https://developer.hashicorp.com/terraform/tutorials/certification-004/associate-study-004

This is graded on two things: does it actually work (`init`/`plan`/`apply`/
`destroy` all succeed), and is it portfolio-quality (clean, commented,
readable, has a README). Don't sacrifice either for speed.

## Structure

```
aws/
├── 01-basics/                    # Obj 2+3 — fundamentals, core workflow
├── 02-variables/                 # Obj 4 — variables
├── 03-outputs/                   # Obj 4 — outputs
├── 04-data-sources/               # Obj 4 — data sources, dependencies
├── 05-modules/                    # Obj 5 — modules
├── 06-state-management/           # Obj 6 — state
├── 07-cli-workspaces/             # Obj 6/7 — CLI `terraform workspace` command
├── 08-functions-expressions/      # Obj 4 — functions, dynamic expressions, type constraints
├── 09-lifecycle-and-validation/   # Obj 4 — lifecycle meta-arg, custom conditions, checks
├── 10-sensitive-data/             # Obj 4 — sensitive variables (+ optional vault provider)
├── 11-maintain-and-troubleshoot/  # Obj 7 — import, state list/show, drift, logs
└── 12-hcp-terraform/              # Obj 8 — HCP Terraform (requires free HCP account)
```

`azure/`, `gcp/`, `okta/`, and `modules/` are planned but not started —
`aws/` is the active track. Don't scaffold those unless explicitly asked.

**Note on naming:** `07-cli-workspaces` was previously named `07-workspaces`.
It was renamed to avoid confusion with `12-hcp-terraform`, since "workspace"
means something completely different in HCP Terraform (a managed remote
execution context) than it does in the CLI (`terraform workspace new/select`,
a way to namespace state files locally). Don't conflate the two when writing
content for either directory.

## Conventions

- Each numbered directory is self-contained and runnable on its own —
  no cross-directory `terraform init` dependencies.
- Each gets its own `README.md` explaining what it demonstrates and how to
  run it (`init` → `plan` → `apply` → `destroy`).
- Use `terraform.tfvars.example` to show variable values. Never commit a
  real `.tfvars` file — it's gitignored.
- Comment code for a portfolio audience: assume the reader knows AWS but
  may be newer to Terraform.
- Standard file split per directory: `main.tf` (provider + resources),
  `variables.tf`, `outputs.tf`. Add more `.tf` files only when a directory's
  topic genuinely needs the separation (e.g. modules will have a
  `modules/` subfolder).

## Current state

Clean slate. No directories under `aws/` exist yet — everything, including
the earlier `01-basics`, was torn down to be rebuilt deliberately, one topic
at a time, as part of a structured study schedule. Don't assume any prior
code exists; check the actual filesystem before referencing what's
"already built."

## Next action

Build out `01-basics/` — provider config, a single `aws_s3_bucket` resource,
and a README walking through the full init/plan/apply/destroy workflow.
This is the first exam objective pair (2: fundamentals, 3: core workflow) —
keep it deliberately simple, nothing from later objectives (variables,
modules, state config) belongs here yet.

## What NOT to do

- Don't jump ahead and scaffold multiple directories at once unless asked —
  this is a study repo, worked through one topic at a time, deliberately.
- Don't add remote backend config or HCP Terraform references to any
  directory before `12-hcp-terraform` — earlier directories should reflect
  the exam objectives they're actually testing, in order.
