# Infrastructure

Documentation for cloud infrastructure, Terraform, and Kubernetes.

## Overview

- **Cloud Provider:** Your cloud provider (e.g. AWS, Azure, GCP)
- **IaC Tool:** Terraform
- **Container Orchestration:** Kubernetes
- **CI/CD:** Your pipeline tool (e.g. GitHub Actions, Azure DevOps)

## Terraform

### Structure

A common pattern is to separate reusable modules from root configurations:

| Repo | Description |
|------|-------------|
| `infra-modules` | Reusable Terraform modules |
| `infra-root` | Root configuration wiring modules together |

### Environments

| Environment | Vars File |
|-------------|-----------|
| dev | `variables_dev.tfvars` |
| qa | `variables_qa.tfvars` |
| prod | `variables_prod.tfvars` |

### Running Terraform Locally

```bash
cd infra-root

terraform init
terraform plan -var-file="variables_dev.tfvars"
terraform apply -var-file="variables_dev.tfvars"
```

### Conventions

- Reusable modules live in their own repos
- Root configurations wire modules together per environment
- Pre-commit hooks should be installed before committing — see the repo README

## Kubernetes

### Useful Commands

```bash
# Switch context
kubectl config use-context <context-name>

# View all pods interactively
k9s

# List Helm releases
helm list -A
```

### Helm Charts

Each application repo contains a `charts/` directory with its Helm chart.

## See Also

- [Runbooks](Runbooks)
- [Getting Started](Getting-Started)
