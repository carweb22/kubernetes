<h1><strong>Deploy Wordpress with Nginx as Loadbalancer, SSL and persistent Volumen</strong></h1><br>
<strong>first you need a working minikube after that you can deploy the cert-manager.yaml</strong><br>

<h1>Install minik k3</h1>

curl -sfL https://get.k3s.io | sh -

<strong>In my installation, there was no configuration file, so I had to copy it.</strong><br>
cp /etc/rancher/k3s/k3s.yaml ~/.kube/config

export KUBECONFIG=~/.kube/config

<strong>Test it</strong><br>
kubectl

<strong>Now to the app!!!</strong>

kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.9.1/cert-manager.yaml

<strong>test cert-manager</strong>
kubectl get pods --namespace cert-manager

<strong>now create this file and the paste the code</strong><br>
letsencrypt-clusterissuer.yaml

k apply -f letsencrypt-clusterissuer.yml

<strong>after deploy the letsencrypt-clusterissuer.yaml now you can create the second file</strong><br>
wordpress.yaml

k apply -f wordpress.yaml

<strong>go to your domain and you will see the wordpress "create new site"</strong>

<strong>I have another app for your kubernetes 'Homarr.' Copy the Homarr code, update the 2 domains in the code, and then deploy it. 😊</strong>
