minikube start

minikube addons enable ingress

minikube tunnel

kubectl create configmap db-init-sql --from-file=init.sql=./sql/insert.sql

kubectl apply -f deployment.yaml

Wait all pods to be ready : kubectl get pods

https://localhost | https://g3-frontend.local (à ajouter au fichier hosts)

Login compte admin

Username : Cessouille
Password : pi

Must have self signed certificate to use the web application.
