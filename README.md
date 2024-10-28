Goal: Kubernetes Wordpress with Nginx as Loadbalancer, SSL and persistent Volumen



kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.9.1/cert-manager.yaml

kubectl get pods --namespace cert-manager

create 
letsencrypt-clusterissuer.yaml

k apply -f letsencrypt-clusterissuer.yml

create 
wordpress.yaml

k apply -f wordpress.yaml
