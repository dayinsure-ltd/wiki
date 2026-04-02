# Terraform

## Structure

| Repo | Description |
|------|-------------|
| `infra-modules` | Reusable modules |
| `infra-root` | Root configuration per environment |

## Environments

| Environment | Vars file |
|-------------|-----------|
| dev | `variables_dev.tfvars` |
| qa | `variables_qa.tfvars` |
| prod | `variables_prod.tfvars` |

## Running Locally

```bash
cd infra-root
terraform init
terraform plan -var-file="variables_dev.tfvars"
terraform apply -var-file="variables_dev.tfvars"
```

## Conventions

- Modules are in their own repos
- Root configs wire modules together per environment
- Install pre-commit hooks before committing — see the repo README

---
[Infrastructure](Infrastructure.md) | [Kubernetes](Infrastructure-Kubernetes.md)
