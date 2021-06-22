# Accessing the Dashboard
 +This will generate a list of all the service names, with their secret name attached.
  + microk8s kubectl -n kube-system get secret
  + To retrieve the secret token for the service in question issue the command: 
  + microk8s kubectl -n kube-system describe secret kubernetes-dashboard-token-fv247

# Service
    +  microk8s kubectl describe svc  -n default

#  set namespace  (default)
    +  kubectl config set "contexts."`kubectl config current-context`".namespace" frontend
    
     
---  
sources: 
 - https://kubernetes.io/docs/reference/kubectl/cheatsheet/

 - https://thenewstack.io/deploy-a-single-node-kubernetes-instance-in-seconds-with-microk8s/