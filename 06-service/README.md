# Load Balancer
- kubectl apply -f 02-service-load-balancer.yaml
- kubectl get service
- kubectl describe service springboot-load-balancer
- Abrir o Postman e fazer a chamada para o seguinte endpoint: http://localhost:8081/v1/users

OBS: se o EXTERNAL-IP não estiver com localhost, pare o Docker e inicialize novamente ou
faça um "reset kubernetes cluster" pela opção setting do Docker

# Cluster IP
- kubectl apply -f 03-service-cluster-ip.yaml
- kubectl get service
- kubectl describe service nginx-cluster-ip
- kubectl run temporary --image=radial/busyboxplus:curl -i --tty
- nslookup springboot-cluster-ip
- curl http://springboot-cluster-ip.default.svc.cluster.local:8082/v1/users


# Node Port
- kubectl apply -f 04-service-node-port.yaml
- kubectl get service
- kubectl describe service springboot-node-port
- kubectl run temporary --image=radial/busyboxplus:curl -i --tty
- nslookup springboot-node-port
- curl http://springboot-node-port.default.svc.cluster.local:8083/v1/users



