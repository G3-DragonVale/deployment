# G3 DragonVale Deployment Guide

## Prerequisites

- [Minikube](https://minikube.sigs.k8s.io/docs/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- Self-signed certificate for HTTPS access

---

## 1. Start Minikube

```sh
minikube start
```

## 2. Enable Ingress

```sh
minikube addons enable ingress
```

## 3. Start Minikube Tunnel

```sh
minikube tunnel
```

## 4. Create Namespace

```sh
kubectl create namespace g3
```

## 5. Create ConfigMap for DB Initialization

```sh
kubectl create configmap db-init-sql --from-file=init.sql=./sql/insert.sql -n g3
```

## 6. Deploy All Resources

```sh
kubectl apply -f deployment.yaml
```

## 7. Wait for All Pods to Be Ready

```sh
kubectl get pods -n g3
```

---

## 8. Access the Application

- [https://localhost](https://localhost)
- [https://g3-frontend.local](https://g3-frontend.local)  
  _(Add `g3-frontend.local` to your hosts file if necessary)_

---

## 9. Admin Login

- **Username:** `Cessouille`
- **Password:** `pi`

---

> **Note:**  
> You must have a self-signed certificate to use the web application.
