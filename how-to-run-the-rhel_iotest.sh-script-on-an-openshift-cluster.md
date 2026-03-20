# How to run the rhel_iotest.sh script on an OpenShift cluster.

Many SAS Viya components require highly performant storage, and SAS generally recommends a sequential I/O bandwidth of 90-120 MB per second, per physical CPU core. Normally this would be achieved by utilizing a storage system that is backed by using SSD or NVMe disks. SAS provides an automated utility script -- rhel_iotest.sh, that uses UNIX/Linux dd commands to measure the I/O throughput of a file system in a Red Hat Enterprise Linux (RHEL) environment. This script can be used to compare the measured throughput of the storage in your environment to the recommendation.

To run a `rhel_iotest.sh` script directly on an OpenShift node, you must access the node's underlying operating system (RHCOS) using `oc debug node/<node_name>`. Once accessed, transfer the script to the node (e.g., via `scp` or `oc cp`), make it executable with `chmod +x`, and run it as root. 

## Steps to Run rhel_iotest.sh on an OpenShift Node
Access the node using a debug container, which provides privileged access to the node's filesystem:
```shell
oc debug node/$(oc get nodes -o name | head -n 1 | cut -d/ -f2)
```
Note: Replace $(...) with your specific node name if necessary.
Switch to the host filesystem to ensure you are running commands on the node, not just inside the debug pod:
```shell
chroot /host
```
Transfer the script to the node. If the script is on your local machine, exit the debug session and use oc cp (from a privileged location):
```shell
oc cp /path/to/rhel_iotest.sh node/<node_name>:/tmp/rhel_iotest.sh
```
Execute the script after re-entering the node:
```shell
chmod +x /tmp/rhel_iotest.sh
/tmp/rhel_iotest.sh
```
 
## Alternative: Running rhel_iotest.sh within a Container 
If the goal is to test IO from a container on a node, use a privileged pod:
```shell
oc run iotest-pod --image=registry.access.redhat.com/ubi9/ubi --privileged -it -- /bin/bash
```

```shell
# Inside the pod:
curl -o rhel_iotest.sh <url_to_script>
chmod +x rhel_iotest.sh
./rhel_iotest.sh
```
