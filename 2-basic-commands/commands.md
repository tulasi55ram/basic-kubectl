### install hyperhit and minikube

`brew update`

`brew install hyperkit`

`brew install minikube`

`kubectl`

`minikube`

### create minikube cluster

`minikube start --vm-driver=hyperkit`

`kubectl get nodes`

`minikube status`

`kubectl version`

### delete cluster and restart in debug mode

`minikube delete`

`minikube start --vm-driver=hyperkit --v=7 --alsologtostderr`

`minikube status`

### check cluster dashboard

`minikube dashboard`

### kubectl create, edit and get pod detials

`kubectl create -h`

- Give Avaibale commands to create pod

`kubectl create deployment nginx-depl --image=nginx`

- Get nginx latest image from docker
- kubectl create deployment NAME --image=image

`kubectl get deployment`

- Get deploment status

`kubectl get pod`

- Get pod status

`kubectl edit deployment nginx-depl`

- Edit auto generated yml file of nginx
- We can increase/decrease replicas
- We can fix image version etc

### kubectl commands

`kubectl get nodes`

`kubectl get pod`

`kubectl get services`

`kubectl get deployment`

`kubectl get replicaset`

### debugging

`kubectl logs {pod-name}`

`kubectl exec -it {pod-name} -- bin/bash`

### create mongo deployment

`kubectl create deployment mongo-depl --image=mongo`

`kubectl logs mongo-depl-{pod-name}`

`kubectl describe pod mongo-depl-{pod-name}`

### delete deplyoment

`kubectl delete deployment mongo-depl`

`kubectl delete deployment nginx-depl`

### create or edit config file

`vim nginx-deployment.yaml`

`kubectl apply -f nginx-deployment.yaml`

`kubectl get pod`

`kubectl get deployment`

### delete with config

`kubectl delete -f nginx-deployment.yaml`

#Metrics

`kubectl top` The kubectl top command returns current CPU and memory usage for a cluster’s pods or nodes, or for a particular pod or node if specified.
