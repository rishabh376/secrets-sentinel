# secrets-sentinel

> Cloud Governance Teams coordinate rotate workload credentials for Kubernetes admission requests, so audit packets are ready before review day.

**Domain:** devsecops | **Complexity:** intermediate | **Stack:** Go, OPA Gatekeeper, Vault, Trivy, Cosign, Falco

| | |
|---|---|
| Use case | Cloud Governance Teams coordinate rotate workload credentials for Kubernetes admission requests, so audit packets are ready before review day. |
| Pain point | Security exceptions linger because ownership and expiry are not enforced. |
| Success metric | Shrink evidence collection from 3 days to 2 hours with complete owner traceability. |
| Cost | $0/mo on Fly.io |

## Why this exists

Security exceptions linger because ownership and expiry are not enforced.. Cloud Governance Teams coordinate rotate workload credentials for Kubernetes admission requests, so audit packets are ready before review day.

> This service shifts security left with scans, signatures, and admission controls so teams can ship safely. For this implementation, the service is designed to remove the operational friction behind Cloud Governance Teams coordinate rotate workload credentials for Kubernetes admission requests, so audit packets are ready before review day..

## What this product does

This project ships a production-oriented service that exposes health, readiness, observability, and domain-specific endpoints for Cloud Governance Teams coordinate rotate workload credentials for Kubernetes admission requests, so audit packets are ready before review day.. The implementation is intended to be deployed behind Kubernetes with secure defaults, CI validation, and rollback-ready manifests.

## Quick start

```bash
docker build -t secrets-sentinel:local .
docker run -p 8080:8080 secrets-sentinel:local
curl http://localhost:8080/healthz
```

## Architecture

```
GitHub CI -> Container Registry -> Kubernetes -> Go -> Operators / SRE
```

See `docs/ARCHITECTURE.md`

## Infrastructure

Full spec: `terraform/INFRA_REQUIREMENTS.md`

TL;DR: K8s cluster, 2-10 pods HPA, $0 on Fly.io

## Docs

- `docs/ARCHITECTURE.md` - components, tradeoffs
- `docs/DESIGN_DISCUSSION.md` - how we decided to build this
- `docs/DEPLOYMENT.md` - GitOps, rollback
- `docs/SECURITY.md` - threat model
- `docs/TROUBLESHOOTING.md` - 3am runbook
- `terraform/INFRA_REQUIREMENTS.md` - **infra: CPU/RAM/storage/cost**

Interview prep: `interview/`
