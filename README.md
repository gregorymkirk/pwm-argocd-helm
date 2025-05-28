# pwm-argocd-helm
helm chart and argoCD app declaraiton to deploy PWM on your cluster.

Tested and functional on EKS, cannot speak to otehr K8S distributions.  Irf you are not using EKS you will deinitely need to create a different storage class that works on your environment.


The storage class should be defined before running the chart, unless you have previously defined a strages class in your EKS cluster that you want to use.  

    kubectl apply -f ./prereqs/storage_class.yaml

The helm chart is deined in ./pwm 

For ArgoCD users: 

application.yaml is a declaritive manifest to create and ArgoCD application tile

    kubectl apply -f ./application.yaml

Helm chart is located in ./pwm  