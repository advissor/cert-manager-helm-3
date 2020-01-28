# Install jetstack cert-manager with Helm 3
5 steps to make launch cert-manager helm chart :)

# High Level steps

1. Install CRDS (CustomResourceDefinition's )
2. Create the namespace for cert-manager
3. Add the Jetstack / Cert-Manager Helm repository
4. Update local Helm repository cache
5. Install the cert-manager Helm chart

# Steps 

```
    kubectl apply --validate=false -f https://raw.githubusercontent.com/jetstack/cert-manager/v0.13.0/deploy/manifests/00-crds.yaml

    kubectl create namespace cert-manager

    helm repo add jetstack https://charts.jetstack.io

    helm repo update

    helm install cert-manager jetstack/cert-manager --namespace cert-manager
```

# Official guide
There is a typo in docs, in the last step, for this purpose I've created this repo

- [cert-manager.io](https://cert-manager.io/docs/installation/kubernetes/)







