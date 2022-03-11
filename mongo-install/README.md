# kubernetes mongodb Manifest YAML's

Kubernetes manifests for mongoDB Deployment.

Full Documentation: Refer https://devopscube.com/deploy-mongodb-kubernetes/ for step by step process to use these manifests.


Adjusted for IBM Cloud demo app. Feel free to inspect the objects and apply them one by one.
Two things are important :
- Update the storageclass in the PVC to the one you want to use
- The deployment assumes dynamic storageclasses (no separate PV is created here)

Quick install is to move into this folder and issue :
kubectl apply -f mongodb-namespace.yaml
kubectl apply -f .

To use the client :
kubectl exec deployment/mongo-client -n icdemo -it -- /bin/bash

on the shell :
mongo --host mongo-svc --port 27017 -u adminuser -p password123