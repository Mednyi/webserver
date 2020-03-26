## Running Kubernetes cluster

1. Run kubernetes cluster with minikube

* `minikube start`

2. Use kubectl to manage and interact with your cluster

* `kubectl get nodes` - list nodes in kluster
* `kubectl ` - list nodes in kluster
* `kubectl create deployment <tag> <image>` - deploy image to cluster
* `kubectl get deployments` - get list of deployments
* `kubectl proxy` - start proxy to directly access kubernetes API
* `kubectl get pods` - list running pods
* `kubectl logs ` - view container logs
* `kubectl exec -it -c <container name> <pod name> <command>` - execute a command in interactive terminal with stdin attached
* `kubectl get <resource name>` - get info about specified resource
* `kubectl describe <resource name>` - get details about resource ex: pod, node , deployment
* `curl http://localhost:8001/api/v1/namespaces/default/pods/<POD_NAME>/proxy/` - route to pod API
* `kubectl expose deployments/<your deployment> --type=<service type> --port <app port>`- create service
* `kubectl label pod <custom label> app=v1` - set new label for pod
* `kubectl get rs` - get replica set
* `kubectl scale deployments/<your deployment> --replicas=n` - scale your deployment to 4 replicas
* `kubectl get pods -o wide` - info about pods and their replicas
