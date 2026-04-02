# Runbooks

Operational procedures for common tasks and incident response.

## Incident Response

### Severity Levels

| Level | Description | Response Time |
|-------|-------------|---------------|
| P1 | Production down / data loss | Immediate |
| P2 | Major feature broken in production | < 1 hour |
| P3 | Minor issue, workaround available | < 4 hours |
| P4 | Low impact / cosmetic | Next sprint |

### Incident Steps

1. Acknowledge the alert
2. Assess severity and assign an owner
3. Create a war-room channel if P1/P2
4. Investigate and apply fix or rollback
5. Communicate status to stakeholders
6. Write a post-mortem for P1/P2 incidents

---

## Deployment Rollback

### Kubernetes / Helm

```bash
# List recent releases
helm history <release-name> -n <namespace>

# Rollback to previous revision
helm rollback <release-name> <revision> -n <namespace>
```

### Terraform

```bash
# Revert to previous state (use with caution)
terraform plan -var-file="variables_prod.tfvars"
# Review, then apply the corrected config
terraform apply -var-file="variables_prod.tfvars"
```

---

## Scaling a Deployment

```bash
# Scale up manually
kubectl scale deployment <name> --replicas=5 -n <namespace>
```

---

## Checking Logs

```bash
# Pod logs
kubectl logs -f <pod-name> -n <namespace>

# Previous container logs (after crash)
kubectl logs <pod-name> -n <namespace> --previous
```

---

## DNS Issues

1. Check your CDN / load balancer routing rules
2. Verify public DNS records are correct
3. Check private DNS zones if using internal services

## See Also

- [Infrastructure](Infrastructure)
