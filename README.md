### To deploy Wordpress, mysql database with persistent volumes
##### create local-volumes.yaml for peristent volumes
```
kubectl create -f local-volumes.yaml
```
we can check persitent volumes by
```
kubectl get pv
kubectl get pvc
```
##### next create wordpress and mysql
```
kubectl create -f wordpress-deployment.yaml
kubectl create -f mysql-deployment.yaml
```

To generate the secret key for validation purpose
```
k create secret generic mysql-pass --from-literal=password=AMuchBetterWay
```
For reference (PluralSight)

```
https://www.udemy.com/kubernetes-from-a-devops-kubernetes-guru/learn/v4/t/lecture/9630332?start=0
```
