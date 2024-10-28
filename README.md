<h1><strong>Deploy Wordpress with Nginx as Loadbalancer, SSL and persistent Volumen</strong></h1><br>
<strong>first you need a working minikube after that you can deploy the cert-manager.yaml</strong><br>

kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.9.1/cert-manager.yaml

<strong>test cert-manager</strong>
kubectl get pods --namespace cert-manager

<strong>now create this file and the paste the code</strong><br>
letsencrypt-clusterissuer.yaml

k apply -f letsencrypt-clusterissuer.yml

<strong>after deploy the letsencrypt-clusterissuer.yaml now you can create the second file</strong><br>
wordpress.yaml

k apply -f wordpress.yaml
