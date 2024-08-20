
<h2 id="kubeadm-setup-prerequisites" class="wp-block-heading has-text-align-center"><span id="Kubeadm_Setup_Prerequisites">Setup Kubernetes Cluster Using Kubeadm [Multi-node]</span></h2>
<p>Following are the prerequisites for <strong>Kubeadm Kubernetes cluster setup</strong>.</p>
</h2>
<p><strong>Kubeadm Kubernetes cluster setup</strong></p>
<ol class="is-style-cnvs-list-styled wp-block-list">
<li>Minimum two <strong>Ubuntu nodes</strong> [One master and one worker node]. You can have more worker nodes as per your requirement. </li>
<li>The master node should have a minimum of <strong>2 vCPU and 2GB RAM</strong>. </li>
<li>For the worker nodes, a minimum of 1vCPU and 2 GB RAM is recommended.</li>
<li><strong>10.X.X.X/X </strong>network range with static IPs for master and worker nodes. We will be using the <strong>192.x.x.x</strong> series as the pod network range that will be used by the Calico network plugin. Make sure the Node IP range and pod IP range don’t overlap.</li>
</ol>

<h2 id="kubernetes-cluster-setup-using-kubeadm" class="wp-block-heading has-text-align-center"><span id="Kubernetes_Cluster_Setup_Using_Kubeadm">Kubernetes Cluster Setup Using Kubeadm</span></h2>
<p>Following are the high-level steps involved in setting up a kubeadm-based Kubernetes cluster.</p>

<ol class="is-style-cnvs-list-styled wp-block-list">
<li>Install container runtime on all nodes- We will be using <a href="https://cri-o.io/" target="_blank" data-type="URL" data-id="https://cri-o.io/" rel="noreferrer noopener">cri-o</a>.</li>
<li>Install Kubeadm, Kubelet, and kubectl on all the nodes.</li>
<li>Initiate Kubeadm control plane configuration on the master node.</li>
<li>Save the node join command with the token.</li>
<li>Install the <a href="https://docs.tigera.io/calico/latest/about/" target="_blank" data-type="link" data-id="https://docs.tigera.io/calico/latest/about/" rel="noreferrer noopener">Calico network plugin</a> (operator).</li>
<li>Join the worker node to the master node (control plane) using the join command.</li>
<li>Validate all cluster components and nodes.</li>
<li>Install Kubernetes Metrics Server</li>
<li>Deploy a sample app and validate the app</li>
</ol>
