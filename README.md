# babs' helm charts

```bash
helm repo add babs https://babs.github.io/helm-charts
```

## babs/extra-objects

```yaml
extraObjects:
  - apiVersion: external-secrets.io/v1beta1
    kind: ExternalSecret
    metadata:
      name: blahblah
    spec:
      secretStoreRef:
        kind: ClusterSecretStore
        name: my-secret-store
      refreshInterval: 1h
      dataFrom:
        - extract:
             key: MY_KEY
```
