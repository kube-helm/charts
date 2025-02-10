# CHART FOR ACCOUNT

## Dependencies
- Using Infisical
- Required `secret` docker registry if using self-host registry
- Required `configmap` infisical

## Add repo
```
helm repo add affiliate-product https://kube-helm.github.io/charts/
```

## Values chart
```
global:
  env: develop | release
  image:
    repository: <repo>
    pullPolicy: Always
    tag: "latest"
  infisical_project_id: <project id in infisical>
  imagePullSecrets:
    - name: registry-affiliate-products
```

## Install chart
```
helm upgrade --install affiliate-product/account
```