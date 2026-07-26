# terraform-portfolio

Hands-on Terraform examples built while studying for the
[Terraform Associate (004)](https://developer.hashicorp.com/certifications/infrastructure-automation)
certification. Each directory is a small, self-contained, runnable example —
not a toy snippet, but not production infrastructure either. The goal is to
demonstrate real understanding of each exam objective, cleanly enough to
show a hiring manager or interviewer.

## Structure

```
terraform-portfolio/
├── aws/              # Active — Terraform Associate 004 study track
│   ├── 01-basics/
│   ├── 02-variables/
│   ├── 03-outputs/
│   ├── 04-data-sources/
│   ├── 05-modules/
│   ├── 06-state-management/
│   ├── 07-cli-workspaces/
│   ├── 08-functions-expressions/
│   ├── 09-lifecycle-and-validation/
│   ├── 10-sensitive-data/
│   ├── 11-maintain-and-troubleshoot/
│   └── 12-hcp-terraform/
├── azure/            # Planned — primary cloud depth, post-certification
├── gcp/               # Planned
├── okta/               # Planned
└── modules/            # Shared reusable modules, used across cloud tracks
```

## Exam objective mapping

| # | Objective | Directory |
|---|---|---|
| 1 | Infrastructure as Code concepts | (conceptual — no code) |
| 2 | Terraform fundamentals | `01-basics` |
| 3 | Core Terraform workflow | `01-basics` |
| 4 | Read, write, modify configuration | `02-variables`, `03-outputs`, `04-data-sources`, `08-functions-expressions`, `09-lifecycle-and-validation`, `10-sensitive-data` |
| 5 | Modules | `05-modules` |
| 6 | Terraform state | `06-state-management`, `07-cli-workspaces` |
| 7 | Maintain infrastructure | `11-maintain-and-troubleshoot` |
| 8 | HCP Terraform | `12-hcp-terraform` |

Full learning path: https://developer.hashicorp.com/terraform/tutorials/certification-004/associate-study-004

## Conventions

- Each numbered directory runs independently: `terraform init` /
  `plan` / `apply` / `destroy` with no cross-directory dependencies.
- Real variable values go in a gitignored `terraform.tfvars`; a
  `terraform.tfvars.example` shows the shape without real values.
- Every directory has its own `README.md`.

## Status

Just getting started. `aws/01-basics` is next up. Working through the
directories in order as part of a structured study schedule.
