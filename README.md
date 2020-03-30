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
* `kubectl run webui-service --image=webui-service --image-pull-policy=Never` - create pod from local docker registry
* `kubectl set image deployments/<your deployment> <previous image> = <updated name>` - set new image for deployment
* `kubectl rollout undo deployments/<your deployment>` - undo last changes
* `kubectl create secret generic <secret name> --from-file=.dockerconfigjson=<absolute path to config.json> --type=kubernetes.io/dockerconfigjson` - create secret for docker registry (need to login first)
* `kubectl get secret ss-secret --output=yaml` - check that secret is created and show it props in yaml format
* `docker build . -t cr.yandex/<repo id>/<image tag>` - build docker image for cr.yandex registry
* `docker push cr.yandex/<repo id>/<image tag>` - push built docker image to registry