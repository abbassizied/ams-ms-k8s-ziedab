# ams-ms-k8s-ziedab

## steps in killercoda:

```sh
$ git clone https://github.com/abbassizied/ams-ms-k8s-ziedab.git
$ kubectl create namespace ams-database 
$ kubectl create namespace ams-backend
$ kubectl create namespace ams-frontend

$ cd ams-ms-k8s-ziedab

# you can see the IP address of each pod with:
$ kubectl get pods -o wide --all-namespaces

$ kubectl apply -f ./mysql 
$ kubectl apply -f ./pma
$ kubectl apply -f ./backend
$ kubectl apply -f ./frontend

$ kubectl get sts -n ams-database
$ kubectl get pods -n ams-database
$ kubectl get svc -n ams-database

$ kubectl get sts -n ams-backend
$ kubectl get pods -n ams-backend
$ kubectl get svc -n ams-backend

$ kubectl get pods -n ams-frontend
$ kubectl get svc -n ams-frontend
```
## services urls:

```sh
/providers/
/articles/
/swagger-ui/index.html
```
## Cleaning up

```sh
$ kubectl delete deployment -l app=xxx
$ kubectl delete service -l app=xxx
$ kubectl delete deployment frontend
$ kubectl delete service frontend

$ kubectl get pods
# The response should look similar to this:
# No resources found in default namespace. 
```
