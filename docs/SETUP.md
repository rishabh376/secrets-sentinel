# Setup - secrets-sentinel

Cloud Governance Teams coordinate rotate workload credentials for Kubernetes admission requests, so audit packets are ready before review day.

1. **Infra first**: `cd terraform && terraform init && terraform apply`
2. `kubectl apply -k k8s/ -n secrets-sentinel`
3. `kubectl port-forward svc/secrets-sentinel 8080:80 -n secrets-sentinel`
4. `curl localhost:8080/healthz`

Env vars: `PORT=8080`, `LOG_LEVEL=info`

Runtime detection and telemetry let us prove the security controls are actually working in prod.
