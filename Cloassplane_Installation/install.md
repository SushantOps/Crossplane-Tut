# To install Crossplane on Kubernetes using Helm, you can follow these steps:

## Install Helm: If you haven't already, you need to install Helm on your local machine or wherever you manage your Kubernetes cluster.

Add the Crossplane Helm repository: Run the following command to add the Crossplane Helm repository to Helm:
```
helm repo add crossplane-stable https://charts.crossplane.io/stable
helm repo update
```

## Install Crossplane: Now, you can install Crossplane using Helm. You can customize the installation by setting various configuration options. Here's a basic installation command:
```
helm install crossplane crossplane-stable/crossplane --namespace crossplane-system
```

This command installs Crossplane into the crossplane-system namespace. You can replace crossplane with any name you prefer for your release.

## Verify installation: After installation, you can verify that Crossplane is running correctly by checking the pods in the crossplane-system namespace:
```
kubectl get pods -n crossplane-system
```

## Accessing the Crossplane dashboard (optional): If you want to access the Crossplane dashboard, you can install the Crossplane dashboard extension using Helm:
```
helm install crossplane-dashboard crossplane-stable/crossplane-dashboard --namespace crossplane-system
```

