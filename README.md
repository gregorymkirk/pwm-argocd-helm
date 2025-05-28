# pwm-argocd-helm
Helm chart and ArgoCD app declaration to deploy PWM on your AWS EKS cluster.

Tested and functional on AWS EKS (1.31), cannot speak to other K8S distributions at this time.  At a minimum you will need to update the ingress controller, and storage class definitions.   




# Pre-Requisites
./prereqs: 
The storage class should be defined before running the chart, unless you have previously defined a storages class in your cluster that you want to use.  Not that this definews a storage clasee or AWS EKS and if you are using a different K8S distribution you will need to create one for your distro.

    kubectl apply -f ./prereqs/storage_class.yaml

# Helm Chart
The helm chart is defined in ./pwm 
example.values.yaml 

# ArgoCD declarative application tile
For ArgoCD users: 

application.yaml is a declaritive manifest to create and ArgoCD application tile

    kubectl apply -f ./application.yaml

Helm chart is located in ./pwm  

Tested and works on:
AWS EKS 1.31 
