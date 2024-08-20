Setup Kubernetes Cluster Using Kubeadm [Multi-node]

Kubeadm Cluster Setup Scripts


Kubeadm Setup Prerequisites
Following are the prerequisites for Kubeadm Kubernetes cluster setup.

Minimum two Ubuntu nodes [One master and one worker node]. You can have more worker nodes as per your requirement.
The master node should have a minimum of 2 vCPU and 2GB RAM.
For the worker nodes, a minimum of 1vCPU and 2 GB RAM is recommended.
10.X.X.X/X network range with static IPs for master and worker nodes. We will be using the 192.x.x.x series as the pod network range that will be used by the Calico network plugin. Make sure the Node IP range and pod IP range don’t overlap.
Note: If you are setting up the cluster in the corporate network behind a proxy, ensure set the proxy variables and have access to the container registry and docker hub. Or talk to your network administrator to whitelist registry.k8s.io to pull the required images.
