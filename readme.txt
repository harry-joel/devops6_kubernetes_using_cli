minikube start --driver=docker
kubectl apply -f nginx-pod.yaml
kubectl get pods
kubectl port-forward pod/nginx-pod 8080:80
kubectl delete pod nginx-pod


kubectl create deployment my-nginx --image=nginx
kubectl get deployments
kubectl scale deployments my-nginx --replicas=3
kubectl expose deployment my-nginx --type=NodePort --port=80
kubectl get svc
minikube service my-nginx --url

