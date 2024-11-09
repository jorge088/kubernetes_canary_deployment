# Kubernetes Canary Deployment

This project contains some basic practice using Kubernets. The objetive is to simulate a deployment environment for the Canary strategy.
Some of the steps followed to rich the objetive are detailed in [Canary Deployment](https://kubernetes.github.io/ingress-nginx/examples/canary/)

# Requisites

* Docker
* Minikube
* Kubectl
* Lens

# Steps

1. Create stable and canary images app version using docker. Go to app version directory and run 'docker build -t app-version'. Then push image into your docker hub repository.
2. In deployments directory, apply deployments for stable and canary version. Remember to edit image in deployment.yaml with your image at docker hub. Run 'kubectl apply -f deployment-version.yaml'. Then check all pods version and services are running with 'kubectl get pods' and 'kubectl get svc'.
3. In deployments directory, apply ingress controller for stable and canary version. Run 'kubectl apply -f ingress-version.yaml'. Then check ingress are running with 'kubectl get ingress'.
4. For localhost we need to add the following in '/etc/hosts' file: '<minikube. ip> minikube.local' . Obtain the minikube ip by runnin 'minikube ip' , this is the IP address of your cluster.