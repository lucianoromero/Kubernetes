https://kubernetes.io/pt-br/docs/concepts/storage/persistent-volumes/
https://kubernetes.io/docs/concepts/storage/volumes/
https://kubernetes.io/blog/2021/09/13/read-write-once-pod-access-mode-alpha/
https://kubernetes.io/docs/concepts/storage/storage-classes/
https://cloud.ibm.com/docs/containers?topic=containers-kube_concepts

- kubectl get pods
- kubectl exec -it <mysql-pod-name> /bin/bash
- mysql -uroot -p
- select user, host from mysql.user;
- UPDATE mysql.user SET host='%' WHERE user='root';
- select user, host from mysql.user;
- exit
- kubectl get pods
- kubectl delete <mysql-pod-name>