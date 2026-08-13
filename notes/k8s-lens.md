# K8s Lens Notes

- Use `kubectl get events --sort-by=.lastTimestamp` to debug recent failures.
- `kubectl top nodes` requires metrics-server; if missing, deploy it via `kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml`.
- For persistent volume claims, check `kubectl describe pvc` for `WaitForFirstConsumer` binding mode.
- Remember to set `--request-timeout=30s` on long-running watches to avoid stale connections.
- Quick cluster context switch: `kubectl config use-context <name>`.

Add more as I learn.