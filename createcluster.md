# Create Cluter Node

 + multipass launch -m 4Gb -n hummingbird-01 (start creating a ubuntu  node)
 + multipass shell hummingbird-01
      + sudo snap install microk8s --classic
        (for specific upstream release series sudo snap install microk8s --classic --channel=1.18/stable)
      + sudo snap install microk8s --classic --channel=1.18/stable  (specific upstream)
      + microk8s status --wait-ready

        Note: In case you get an insufficient permissions message, you need to use the following commands to add ‘ubuntu’ user to the microk8s sudoers group inside the VM:

        sudo usermod -a -G microk8s ubuntu
        sudo chown -f -R ubuntu ~/.kube


 + Now let’s focus on creating the Kubernetes cluster. On the initial node, run:
      + microk8s add-node       

 + Create or Delete a namespace
      + microk8s kubectl create ns object-matrix-ns
      + microk8s kubectl delete ns object-matrix-ns     