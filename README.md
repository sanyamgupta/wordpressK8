Config check:- Create a docker-compose file an run containers to check configuration before deploying to kubernetes.

steps to deploy:- 
Create a K8 cluster. 

Run following commands in k8 cluster

helm repo add stable https://kubernetes-charts.storage.googleapis.com/
helm repo update
helm install nginx-ingress stable/nginx-ingress

kubectl create -f wordpress.yaml
kubectl create -f mysql.yaml

echo "68.183.245.253 wordpress.stackexpress.com" | sudo tee -a /etc/hosts

Access:-
wordpress.stackexpress.com
