# pwm-argocd-helm
Helm chart and ArgoCD app declaration to deploy PWM on your K8S cluster.

Tested and functional on AWS EKS (1.31), cannot speak to otehr K8S distributions at this time.  I you use this with a differnmt version of distributioin of K8S and it works please either add it to the bottom this readme 


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
