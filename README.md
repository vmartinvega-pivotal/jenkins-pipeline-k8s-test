Install minikube

```
git clone  https://github.com/vmartinvega-pivotal/jenkins-pipeline-k8s-test
```


configure the config file (to connect to kubernetes) to emmbed the certificates
Configure cloud in jenkins
Configure secret from file (the previously created file)
Jenkins url (internal ip for the pod) and port 8080
Jenkins tunnel (internal ip for the pod) and port 50000
Test connectivity

Create pipeline from source control


Copy Dockerfile to minikube to build the jenkins image
```
docker build -t vicente/jenkins-image:1.0 .
```

Create the jenkins deployment
```
kubectl create -f jenkis-deployment.yaml
```

Create the jenkins service
```
kubectl create -f jenkins-service.yaml
```

Configure jenkins web to be displayed in english
```
Jenkins -> Configure -> Locale (en_EN)
```

Configure cloud
