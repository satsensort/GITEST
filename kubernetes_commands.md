

Imperative Commands:
======================
Kubernetes Create a Service Type LoadBalancer apply to deployment
======================================================================
# kubectl expose deployment nginx --type=LoadBalancer --name=nginx-service --port=80 --target-port=80 

Create a Nginx Deployment
===========================
# kubectl run nginx --image=nginx:latest 

## It creates deployment, Replica sets and pods automatically, If we dont want the deployment to be created use --generator=run-pod/v1