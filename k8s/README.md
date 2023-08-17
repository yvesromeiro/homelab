# K8S

**Add Network to pods**

```
# Needs manual creation of namespace to avoid helm error
kubectl create ns kube-flannel
kubectl label --overwrite ns kube-flannel pod-security.kubernetes.io/enforce=privileged

helm repo add flannel https://flannel-io.github.io/flannel/
helm install flannel --set podCidr="10.10.0.0/16" --namespace kube-flannel flannel/flannel
```

**Access services local**

```
kubectl port-forward -n monitoring svc/grafana 33000:3000
kubectl port-forward -n monitoring svc/prometheus-k8s 39090:9090
kubectl port-forward -n monitoring svc/alertmanager-main 39093:9093
```
