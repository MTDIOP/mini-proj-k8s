# mini-proj-k8s
kubectl create -f pv.yaml

persistentvolume/mysql-pv-mp created

kubectl create -f pvc.yaml

persistentvolumeclaim/mysql-pv-mp-claim created

kubectl create -f mysql-deployment.yaml

deployment.apps/mysql created

kubectl create -f service-mysql.yml 

service/service-mp-mysql created

kubectl apply -f wordpess.yaml 

deployment.apps/wordpress created

kubectl create -f service-wordpress.yml

service/service-mp-wordpress created
