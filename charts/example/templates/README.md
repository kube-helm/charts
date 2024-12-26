# Templates

## POD
In Kubernetes, a pod is considered the smallest unit that can be deployed. It can consist of one or a group of containers that share the same execution environment.
- Only IP address in the Kubernetes cluster.
- Can hold multiple containers.
- These containers share the same IP with each other, distinguished by port; Containers of the same pod can call each other via localhost, and calls to containers in another pod must include an IP.

## Services
- File: service.yaml
- Acts as the entry point to a set of other pods that provide the same feature or service. This resource is responsible for coordinating and balancing the load between connected pods.
- Example: [Detail](https://github.com/trunglt251292/k8s-helm-chart/blob/master/example/templates/service.yaml))

## Ingress
- File: ingress.yaml
- Ingress is a Kubernetes resource that allows routing of HTTP Loadbalancer configurations for applications running on Kubernetes, represented by one or more Services. Such a loadbalancer is needed to make those applications available to clients like the browser we access outside of the Kubernetes cluster.
    - Example:
        Service A -> https://domain.com/a
        Service B -> https://domain.com/b
- Example: [Detail](https://github.com/trunglt251292/k8s-helm-chart/blob/master/example/templates/ingress.yaml)

## Deployments
- File: deployment.yaml
- Deployment is a resource of kubernetes that helps us in updating a new version of an application easily, it provides two deployment strategies: Recreate and RollingUpdate, all of which are done automatically below, and different versions. deployed will have a history in the background, you can rollback and rollout between versions at any time without re-running CI/CD.
- When we create a Deployment, it will create a ReplicaSet underneath, and the ReplicaSet will create a Pod. Follows:
    - Deployments -> Replicaset -> Pods
- Example: [Detail](https://github.com/trunglt251292/k8s-helm-chart/blob/master/example/templates/deployment.yaml)

## HPA
