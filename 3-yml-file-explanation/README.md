# Apply yml files

`kubectl apply -f nginx-deployment.yml`

`kubectl apply -f nginx-service.yml`

`kubectl get pod`

`kubectl get deployments`

`kubectl get service`

`kubectl describe service {service-name}`

- Check end points, targetPort, Name, Annotations, Type

`kubectl get pod -o wide`

- Get more information on pods

`kubectl get deployment nginx-deployment -o yaml`

- Get yaml format pod details

`kubectl get deployment nginx-deployment -o yaml > nginx-deployment-result.yml`

- Store status of pod details in kubernetes

`kubectl delete -f nginx-deployment.yml`
`kubectl delete -f nginx-service.yml`

- Delete nginx deployment and services
