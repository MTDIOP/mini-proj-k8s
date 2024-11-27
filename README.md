# mini-proj-k8s
----------------------------Create namespace ---------------------

kubectl create namespace production

![alt text](images/namespace.png)

----------------------------Create PV ---------------------

kubectl create -f pv.yaml -n production

persistentvolume/mysql-pv-mp created

![alt text](images/pv.png)

----------------------------Create PVC ---------------------

kubectl create -f pvc.yaml -n production

persistentvolumeclaim/mysql-pv-mp-claim created

![alt text](images/pvc.png)

----------------------------Mysql & Wordpress deployement---------------------

kubectl create -f mysql-deployment.yaml -n production

deployment.apps/mysql created

kubectl apply -f wordpess-deployment.yaml -n production

deployment.apps/wordpress created

![alt text](images/deployments-services.png)

----------------------------Mysql  & Wordpress Services----------------------

kubectl create -f service-mysql.yml -n production

service/service-mp-mysql created

kubectl create -f service-wordpress.yml -n production

service/service-mp-wordpress created

![alt text](images/services.png)

----------------------------Connexion à l'application----------------------------

![alt text](images/appli_access.png)