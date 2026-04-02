# Kubernetes

## Common Commands

```bash
# Switch cluster context
kubectl config use-context <context-name>

# Open interactive terminal UI
k9s

# List all Helm releases
helm list -A

# View pod logs
kubectl logs -f <pod-name> -n <namespace>

# Scale a deployment
kubectl scale deployment <name> --replicas=3 -n <namespace>
```

## Helm Charts

Each application repo has a `charts/` directory containing its Helm chart.

To upgrade a release:

```bash
helm upgrade <release-name> ./charts/<chart-name> -n <namespace> -f values.yaml
```

To roll back:

```bash
helm history <release-name> -n <namespace>
helm rollback <release-name> <revision> -n <namespace>
```

---
[Infrastructure](Infrastructure) | [Terraform](Infrastructure-Terraform)
