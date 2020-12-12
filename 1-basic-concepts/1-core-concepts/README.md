# k8s core concepts

- pod
- services
- ingress
- volumes
- configMap
- secrets
- deployment
- statefulSet

# Services

- communication between pods

# Ingress

- Route traffic into k8s cluster

# ConfigMap

- Define DB_URLS and other info

# Secrets

- Define DB Username and passwords

# Volumes

- Data persistence (Store on local or remote, outside of k8s cluster)
- K8s doesn’t manage data persistence!

# Deployment

- StateLessSet
- Pod blueprint.
- Replicating pod.
- Only useful for web application.
- Not for Databases.

# StatefulSet

- Useful for DBs
- MysqL, MongoDB created using stateful set not with deployment.

`Deployment of StatefulSet application in k8s is not easy.`
`DBs are often hosted outside of k8s cluster.`
