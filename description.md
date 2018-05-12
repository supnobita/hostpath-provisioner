# Project Description
This is a hostpath dynamic provisioner for kubernetes. I create this project for my kubernetes cluster which use NFS (lizardfs) as a storage backend and use this to enable dynamic provision persistent volume. First I mount /data nfs-server/exporter, then I start Pod which will (create PV and create dir in /data). 
## Setup steps
1) mount nfs folder
2) Create DaemonSet (to run hostpath-provisioner on every node in Kubernetes)
3) Create RBAC
4) Create Clame and test pod
