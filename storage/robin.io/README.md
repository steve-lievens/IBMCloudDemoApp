Using Robin.io as storage in this demo
======================================

To use robin.io as storage, make sure to use "robin" as storageclass in any PVC being used.

If you need to take a snapshot of this volume, you need to create the snapshotclass on your cluster first.
The yaml is included in this folder.

kubectl create -f robin-snapshotclass.yaml

To check if it was applied :

kubectl get volumesnapshotclass

