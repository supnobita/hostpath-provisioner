# Project Description
This is a hostpath dynamic provisioner for kubernetes. I create this project for my kubernetes cluster which use NFS (lizardfs) as a storage backend and use this to enable dynamic provision persistent volume. First I mount /data nfs-server/exporter, then I start Pod which will (create PV and create dir in /data). 
## Setup steps
1) mount -t nfs /data _NFS_IP:/nfs/export #mount nfs export to /data folder
2) kubectl apply -f hostpath-allinone.yaml
3) create a claim with storage-class: "hostpath"
