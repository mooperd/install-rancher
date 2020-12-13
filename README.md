# Installing Rancher on Kubernetes

Make sure you have the most recent version of helm installed.

```
helm repo add rancher-latest https://releases.rancher.com/server-charts/latest
helm template rancher rancher-latest/rancher --namespace cattle-system --set useBundledSystemChart=true --set hostname=rancher.my.org --set tls=external > rancher.yaml
kubectl create namespace cattle-system
kubectl apply -f rancher.yaml -n cattle-system
```

