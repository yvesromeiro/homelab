# K8S

**Access services local**

```
kubectl port-forward -n monitoring svc/grafana 33000:3000
kubectl port-forward -n monitoring svc/prometheus-k8s 39090:9090
```
