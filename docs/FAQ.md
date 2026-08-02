# FAQ - secrets-sentinel

**Q: What problem does this actually solve?**
A: Cloud Governance Teams coordinate rotate workload credentials for Kubernetes admission requests, so audit packets are ready before review day.

Pain point: Security exceptions linger because ownership and expiry are not enforced.

**Q: Free to run?**
A: Yep. Fly.io - $0/mo. See `terraform/INFRA_REQUIREMENTS.md`

**Q: Production ready?**
A: Yes - SLOs, security hardening, DR runbook, Helm, Terraform, monitoring.

**Q: Stack?**
A: Go, OPA Gatekeeper, Vault, Trivy, Cosign, Falco

**Q: What infra do I need?**
A: `terraform/INFRA_REQUIREMENTS.md` has the full breakdown - CPU/RAM/storage/network/cost.
