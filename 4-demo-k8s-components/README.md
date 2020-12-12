# Demo Mognodb and mongoExpress using k8s components

- DB_URL using configMap
- DB_USERNAME and DB_PASSWORD using secret
- MongoDB pod
- MongoExpress pod
- Environment variables in deployment.yaml
- internal service (Mogodb to mongo express)
- external service (access mongo express using url)

# Refer application.drawio for end to end control flow

# Stages

- Create deployment pod for MongoDB using mongo.yaml file
- Create mongo-secrets.yaml to store db username and password
- Apply mongo-secrets.yaml file
- Add valueFrom value for username and password in mongo.yaml file
- Apply mongo.yaml file
- Create mongodb internal service as seperate file or with in mongo.yaml file by adding 3 columns.
- Apply mongo.yaml file (Contains internal service)
- Create mongo-express.yaml file
- Create mongo-config.yaml file
- Apply mongo-config.yaml file and then mongo-express.yaml
- create external service inside of mongo-express.yaml file ( it is same as internal servier but adding type: loadbalener and nodeport it will become external service)
- `kubectl get service` command gives mongo-express-service type as loadBalencer.
- Since we are working on minicube, it shows external-ip as pending.
- To get external ip then enter `minikube service {service-name}` command

# mongo.yaml file

- contains mongo image with version 4.4
- uses username and password from mongo-secrets.yaml file

# mongo-secrets.yaml file

- define all secrets username and password
- use base64 encoded values and from terminal you can generate base64 encoded values
- echo -n 'root' | base64
