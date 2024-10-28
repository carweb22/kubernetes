<h1><strong>Deploy Wordpress with Nginx as Loadbalancer, SSL and persistent Volumen</strong></h1>
<p>first you need a working minikube</p>

kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.9.1/cert-manager.yaml

kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.9.1/cert-manager.yaml

kubectl get pods --namespace cert-manager

<p>now create this file and the paste the code</p>
letsencrypt-clusterissuer.yaml

k apply -f letsencrypt-clusterissuer.yml

<p>after deploy the letsencrypt-clusterissuer.yaml now you can create the second file</p> 
wordpress.yaml

k apply -f wordpress.yaml
