---
apiVersion: v1
kind: PersistentVolume
metadata:
  annotations:
    volume.beta.kubernetes.io/storage-class: "default"
  name: bitcoind-pv
  labels:
    name: bitcoind-pv
spec:
  awsElasticBlockStore:
    fsType: ext4
    volumeID: <please-change-me>
  accessModes:
    - ReadWriteOnce
  capacity:
    storage: 400Gi
---
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  annotations:
    volume.beta.kubernetes.io/storage-class: default
  name: bitcoind-pvc
spec:
  resources:
    requests:
      storage: 400Gi
  accessModes:
    - ReadWriteOnce
  selector:
    matchLabels:
      name: bitcoind-pv
