# Deployment
Using helm for our kubernetes deployments/applications

## Database Deploy
Using patroni kubernetes config in order for the HA Postgre to be accomplished

### How to execute
```
cd challenges/challenge-devops/helm
kubectl create ns psql-spilo-test
helm upgrade --install db-deploy db-deploy --force
```

## RoR Deploy
Encapsulating RoR deployment using docker and kubernetes

### How to execute
```
cd challenges/challenge-devops/
docker build -t ruby-client .
cd helm
kubectl create ns ruby-client-demo
helm upgrade --install db-deploy db-deploy --force
```

## Nginx Controller
This will set a base for the routing of our applications, in this we can add or modify existing cluster routes, ssl keys, domain routing, etc...

For the sake of demonstration we only just did a bare configuration in order for things to run and execute

### How to execute
```
cd challenges/challenge-devops/helm
kubectl create ns k8s-nginx-ingress
helm upgrade --install k8s-nginx-ingress k8s-nginx-ingress --force
```

