# mini-proj-k8s
----------------------------Create PV ---------------------
kubectl create -f pv.yaml

persistentvolume/mysql-pv-mp created

![alt text](images/pv.png)
----------------------------Create PVC ---------------------

kubectl create -f pvc.yaml

persistentvolumeclaim/mysql-pv-mp-claim created

![alt text](images/pvc.png)

----------------------------Mysql & Wordpress deployement---------------------

kubectl create -f mysql-deployment.yaml

deployment.apps/mysql created

kubectl apply -f wordpess.yaml 

deployment.apps/wordpress created

![alt text](images/deployments-services.png)

----------------------------Mysql  & Wordpress Services----------------------

kubectl create -f service-mysql.yml 

service/service-mp-mysql created

kubectl create -f service-wordpress.yml

service/service-mp-wordpress created

![alt text](images/services.png)

----------------------------Exposition du port ----------------------------

![alt text](images/image-1.png)

----------------------------Connexion à l'application----------------------------

![alt text](images/appli_access.png)