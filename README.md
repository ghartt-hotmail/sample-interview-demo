README
### Pre-requisites and software installations needed to deploy app/cluster

Digital ocean cmd line and authentication
doctl install:
[How to Install and Configure doctl | DigitalOcean Documentation](https://docs.digitalocean.com/reference/doctl/how-to/install/)

### git install required to create repository
[Git - Downloading Package](https://git-scm.com/downloads/win)

### docker desktop install required to containerize application
[Windows Docker Docs](https://docs.docker.com/desktop/setup/install/windows-install/)

### install k8s tools to work with the Digital Ocean cluster
https://kubernetes.io/docs/tasks/tools/


fork repo of sample application
https://www.digitalocean.com/community/tutorials/automating-birthday-reminders-with-triggers
digitalocean/sample-nodejs: ⛵ App Platform sample Node.js application.

Run the following docker commands from a terminal to containerize the application:
docker init
node.js version 24.5
yarn
yarn start
port 3000

docker compose up --build
push image to hub

## Digital Ocean console / control panel
## App Platform
authorize GitHub 
select repo for deployment

Dedicated instance sizes starting at $29.00/mo can enable autoscaling.
Cost saving measure

create container registry in Digital Ocean

dependency free registration
https://docs.digitalocean.com/products/container-registry/how-to/use-registry-docker-kubernetes/#option-2-use-credentials-obtained-from-the-control-panel

doctl auth init

doctl registry login -- enable container images to be used by App

## create k8s cluster, allow auto-scale

back to cluster

doctl kubernetes cluster kubeconfig save 8d739f57-ebec-4d79-8a1e-dc9a408c0da8

Notice: Adding cluster credentials to kubeconfig file found in "C:\\Users\\ghart\\.kube\\config"
Notice: Setting current-context to do-sfo3-k8s-sample-interview-demo

kubectl config get-contexts
Lists your cluster name, user, and namespace
kubectl cluster-info
Display addresses of the control plane and cluster services
kubectl version
Display the client and server k8s version
kubectl get nodes
List all nodes created in the cluster
kubectl help






Add load balancer
How to Add Load Balancers to Kubernetes Clusters | DigitalOcean Documentation



https://docs.digitalocean.com/products/kubernetes/how-to/connect-to-cluster/#download

PS C:\Users\ghart\.kube> kubectl --kubeconfig=k8s-sample-interview-demo-kubeconfig.yaml get nodes
NAME                               STATUS   ROLES    AGE   VERSION
sample-interview-demo-pool-27f33   Ready    <none>   15h   v1.33.1
sample-interview-demo-pool-27f38   Ready    <none>   15h   v1.33.1
sample-interview-demo-pool-27f3n   Ready    <none>   15h   v1.33.1
PS C:\Users\ghart\.kube>


