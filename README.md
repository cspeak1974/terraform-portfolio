# Terraform Portfolio

Hands-on Terraform study and portfolio project demonstrating progressive skills across multiple cloud providers. Also serves as exam prep for **Terraform Associate (004)**.

## Structure

| Directory | Status | Description |
|-----------|--------|-------------|
| [aws/](aws/) | Active | AWS provider — basics through advanced patterns |
| [azure/](azure/) | Planned | Azure provider (primary cloud depth) |
| [gcp/](gcp/) | Planned | Google Cloud provider |
| [okta/](okta/) | Planned | Okta provider |
| [modules/](modules/) | Planned | Shared reusable modules |

## AWS Sections

| Section | Topic |
|---------|-------|
| [01-basics](aws/01-basics/) | Providers, resources, `terraform init/plan/apply` |
| [02-variables](aws/02-variables/) | Input variables, types, validation |
| [03-outputs](aws/03-outputs/) | Output values, `terraform output` |
| [04-data-sources](aws/04-data-sources/) | Data sources, reading existing infrastructure |
| [05-modules](aws/05-modules/) | Module creation and composition |
| [06-state-management](aws/06-state-management/) | Remote state, backends, state locking |
| [07-workspaces](aws/07-workspaces/) | Workspaces for environment separation |

## Conventions

- Terraform >= 1.12
- `.tfvars` files are gitignored — copy `.tfvars.example` and fill in values
- Each directory is self-contained and independently runnable
- Numbered directories show skill progression
