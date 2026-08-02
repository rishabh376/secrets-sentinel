# Operations Runbook - secrets-sentinel

Cloud Governance Teams coordinate rotate workload credentials for Kubernetes admission requests, so audit packets are ready before review day.

**On-call? Read this first.**

## Deploy
```
kubectl apply -k k8s/ -n secrets-sentinel
kubectl rollout status deploy/secrets-sentinel -n secrets-sentinel
```

## Rollback (when things go red)
```
./scripts/rollback.sh
# usually < 30sec
```

## Scale up NOW
```
kubectl scale deploy/secrets-sentinel --replicas=10 -n secrets-sentinel
```

## Logs
```
kubectl logs -l app=secrets-sentinel -n secrets-sentinel -f --tail=200
```

## Crashloop?
```
kubectl describe pod -l app=secrets-sentinel -n secrets-sentinel
kubectl logs <pod> --previous -n secrets-sentinel
```
90% of the time: missing env var in ConfigMap.

## Metrics
`curl localhost:8080/metrics` or Grafana dashboard in `monitoring/`

## DR / Failover
See `docs/DISASTER_RECOVERY.md` - RTO 15m

We actually tested this. 11 min.
