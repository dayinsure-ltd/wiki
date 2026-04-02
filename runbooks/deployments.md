# Deployments

## Deploying via CI/CD

All deployments should go through the pipeline. Avoid manual deploys to production.

## Rolling Back — Helm

```bash
# List release history
helm history <release-name> -n <namespace>

# Roll back to a previous revision
helm rollback <release-name> <revision> -n <namespace>
```

## Rolling Back — Terraform

Revert the change in source control, raise a PR, and let the pipeline apply it.

If an emergency manual rollback is needed:

```bash
terraform plan -var-file="variables_prod.tfvars"
terraform apply -var-file="variables_prod.tfvars"
```

## Checking Logs After a Deploy

```bash
# Live pod logs
kubectl logs -f <pod-name> -n <namespace>

# Logs from a crashed container
kubectl logs <pod-name> -n <namespace> --previous
```

---
[Runbooks](README.md) | [Incident Response](incident-response.md)
