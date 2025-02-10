# CHART FOR COMMON

## Dependencies
- Using Infisical
- Required `secret` docker registry if using self-host registry
- Required `configmap` infisical

## Add repo
```
helm repo add affiliate-product 
```

## Values chart
```
global:
  env: develop | release
  image:
    repository: <repo>
    pullPolicy: IfNotPresent
    tag: "latest"
  infisical_project_id: <project id in infisical>
  imagePullSecrets:
    - name: registry-affiliate-products
```

## Install chart
```
helm upgrade --install affiliate-product/common
```