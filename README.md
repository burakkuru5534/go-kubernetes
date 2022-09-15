# go-kubernetes

#$ go build
#$ ./go-kubernetes

#create Dockerfile
#$ docker build -t go-kubernetes .
#$ docker tag go-kubernetes burakkuru5534/go-hello-world:1.0.0
#$ docker login
#$ docker push burakkuru5534/go-hello-world:1.0.0

#create kubernetes deployment file (.yml)
#$ minikube start
#$ kubectl apply -f k8s-deployment.yml

#$ kubectl get deployments
#$ kubectl get pods
#We can use the kubectl port-forward command to map a local port to a port inside the pod like this:
#$ kubectl port-forward go-hello-world-69b45499fb-7fh87 8080:8080

#$ kubectl logs -f go-hello-world-69b45499fb-7fh87

#create kubernetes service
#kubectl apply -f k8s-deployment.yml (we can update this yml or create another yml file)

#$ kubectl get services

#Type the following command to get the URL for the service in the minikube cluster:
#$ minikube service go-hello-world-service --url

#scale a kubernetes deployment

#$ kubectl scale --replicas=4 deployment/go-hello-world

#delete a kubernetes deployment

#$ kubectl delete deployment go-hello-world

#delete a kubernetes service

#$ kubectl delete service go-hello-world-service

#delete a pod

#$ kubectl delete pod go-hello-world-69b45499fb-7fh87
