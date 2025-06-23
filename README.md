minikube start

minikube addons enable ingress

minikube tunnel

kubectl create namespace g3

kubectl create configmap db-init-sql --from-file=init.sql=./sql/insert.sql -n g3

kubectl apply -f deployment.yaml

Wait all pods to be ready: kubectl get pods -n g3

https://localhost | https://g3-frontend.local (add to hosts file if necessary)

Login admin account

Username: Cessouille
Password: pi

Must have self signed certificate to use the web application.
