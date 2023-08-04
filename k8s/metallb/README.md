# Bare Metal Load Balancer

OBS: I'm using weave networks

**Instal first from manifest**

```
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.13.9/config/manifests/metallb-native.yaml
```

**than apply the configuration of network**

```
kubectl apply -f addressPool.yaml
kubectl apply -f l2advertisement.yaml
```

