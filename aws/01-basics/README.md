# 01 — Basics

Core Terraform workflow: configure a provider, declare a resource, and run `init → plan → apply → destroy`.

## What This Covers

- `terraform` block with required providers and version constraints
- `provider` block configuration
- Declaring an `aws_instance` resource
- Running the Terraform CLI workflow
- Reading plan output

## Prerequisites

- AWS credentials configured (`aws configure` or environment variables)
- Terraform >= 1.12 installed

## Usage

```bash
cp terraform.tfvars.example terraform.tfvars
# edit terraform.tfvars with your values

terraform init
terraform plan
terraform apply
terraform destroy
```

## Files

| File | Purpose |
|------|---------|
| `main.tf` | Provider and resource declarations |
| `terraform.tfvars.example` | Example variable values (copy to `terraform.tfvars`) |
