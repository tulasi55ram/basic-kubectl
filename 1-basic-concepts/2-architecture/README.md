# Basic Architecture of k8s

# Master and Slaves architecture

- Each node contain multiple pods.
- K8s cluster contain multiple nodes and each node should have “container run time “.

# Each worker node should contain 3 process

- Kubectl
- Kube proxy
- Container run time

# Master node should contain 4 processes

- Api server
- Scheduler
- Controller manager
- Etcd

# Api server

- Cluster gateway (get initial request)
- Acts as gatekeeper for authentication. Only authorised requests
- Some request -> API server -> Validate request -> other processes -> pod

# Scheduler

- It has intelligence where to put pod (Which node)
- Schedule new pod -> API server -> Scheduler -> where to put pod! ->Kubelets(on worker nodes)

# Controller manager

- Detects the cluster state changes (If any pod destroyed then controller manager immediately knows).
- Controller manager -> Scheduler -> kubelet -> pod

# Etcd

- Brain of k8s cluster
- Etcd get stored as key value pair
- Application data not stored.
- Every changes in cluster stored/updated in etcd (For example new pod get dies and new pod get created).
