minikube start --driver docker
minikube status
kubectl get node

kubectl apply -f mongo-config.yaml
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo.yaml
kubectl apply -f webapp.yaml

kubectl get all

kubectl [command] --help

kubectl describe [component_type] [component_name] 
kubectl describe service webapp-service
kubectl describe pod pod/mongo-deployment-57ffcb654d-7g674

kubectl logs [pod_name]
kubectl logs [pod_name] -f # steam the log

kubectl get svc
minikube ip **or** kubectl get node -o wide # where *-o wide* output more detailed info