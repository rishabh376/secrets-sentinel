# Deployment - secrets-sentinel

**Use case:** Cloud Governance Teams coordinate rotate workload credentials for Kubernetes admission requests, so audit packets are ready before review day.

## Infra requirements
→ `terraform/INFRA_REQUIREMENTS.md` - CPU/RAM/storage/network/cost breakdown

## GitOps
Flux watches `main` and reconciles changes automatically.

## Rollback
```
./scripts/rollback.sh
kubectl rollout undo deploy/secrets-sentinel -n secrets-sentinel
```
Usually < 30 sec.

## Cost
Fly.io - $0/mo

The focus is supply-chain hardening: SBOMs, Cosign signatures, and policy enforcement across build and deploy.
