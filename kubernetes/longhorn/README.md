# Install
Only support arm64 so you need to be running the RaspiOS 64bit release (linux/arm64)

## Helm
```
helm repo add longhorn https://charts.longhorn.io
helm repo update

kubectl create namespace longhorn-system
helm install longhorn longhorn/longhorn --namespace longhorn-system
```

Confirm if it's working:
```
kubectl -n longhorn-system get pod
```