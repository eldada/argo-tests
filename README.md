# Trying out ArgoCD
This repository is a simple example for trying out [Argo CD](https://argo-cd.readthedocs.io/) with a Kubernetes cluster

## Install
- Have access to a Kubernetes cluster (with full admin privileges)
- Install with instructions from [Argo getting_started](https://argo-cd.readthedocs.io/en/stable/getting_started/) guide
- Access the [Argo CD UI](https://argo-cd.readthedocs.io/en/stable/getting_started/#3-access-the-argo-cd-api-server)

## Create the applications 
- [simple-yaml](apps/simple-yaml) - a single pod example
- [simple-helm](apps/simple-helm) - a demo helm chart (nginx created by `helm create demo`)
- Apply the applications definitions yaml from command line
```shell
kubectl apply -f applications/simple-yaml.yaml
kubectl apply -f applications/simple-helm.yaml
```
- See the applications are created in Argo UI
- See the objects are created in the Kubernetes cluster (pods, services, configmaps etc.)

## Update an application
- Make a change to any of the provided example applications ([simple-helm](apps/simple-helm) for example)
- Commit and push the change
- View application being synced in the UI

## More examples
See more examples in the [ArgoCD examples repository](https://github.com/argoproj/argocd-example-apps)
