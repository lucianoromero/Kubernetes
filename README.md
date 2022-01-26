# Workshop Mão na Massa de Kubernetes para iniciantes
Introduction Kubernetes

Install -> Releases v1.23.2
https://github.com/kubernetes/minikube/releases/tag/v1.23.2

https://kubernetes.io/docs/tasks/run-application/run-single-instance-stateful-application/
https://phoenixnap.com/kb/kubernetes-mysql
https://www.magalix.com/blog/kubernetes-and-database

mysql -u root -ppassword

use mysql;
UPDATE user SET host='%' WHERE user='root' AND host='localhost';
FLUSH PRIVILEGES;

kubectl run -it --rm --image=mysql/mysql-server:latest --restart=Never mysql-client -- mysql -h mysql -ppassword
select user, host from mysql.user;

https://stackoverflow.com/questions/66860306/k8s-local-persistent-volume-on-docker-desktop-loses-data-after-docker-desktop-re
