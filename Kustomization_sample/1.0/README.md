
# Kustomization sample project

- created sample-app with given files and directory structure

```text
tree /F
Folder PATH listing for volume Data
Volume serial number is 5A8D-9F5E
D:.
├───base
│   │   kustomization.yaml
│   │
│   └───nginx
│           deployment.yaml
│           kustomization.yaml
│
└───overlays
    └───staging
            deploymentPatchA.yaml
            kustomization.yaml
```

- Use the oc apply -k command to deploy the application with Kustomize
```text
kubectl apply -k base
```

- deploy staging overlay that increase number of replicas and cpu of the deployment.
```text
kubectl apply -k overlays/staging
```