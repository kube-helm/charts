# Example helm with nodejs express

## Build docker image
- Dùng docker hub
- Push image

## Structure
- Templates:
  - Template files should have the extension .yaml if they produce YAML output. The extension .tpl may be used for template files that produce no formatted content.
  - Template file names should use dashed notation (my-example-configmap.yaml), not camelcase.
  - Each resource definition should be in its own template file.
  - Template file names should reflect the resource kind in the name. 
- Charts
  - Helm uses a packaging format called charts. A chart is a collection of files that describe a related set of Kubernetes resources. A single chart might be used to deploy something simple, like a memcached pod, or something complex, like a full web app stack with HTTP servers, databases, caches, and so on.
  - Charts are created as files laid out in a particular directory tree. They can be packaged into versioned archives to be deployed.
- Values
  - This part of the best practices guide covers using values. In this part of the guide, we provide recommendations on how you should structure and use your values, with focus on designing a chart's values.yaml file.