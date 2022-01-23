# https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale-walkthrough/
https://blog.codewithdan.com/enabling-metrics-server-for-kubernetes-on-docker-desktop/

- https://k8s.io/examples/application/php-apache.yaml

# Comandos
- kubectl apply -f 01-metrics-deployment.yaml
- kubectl apply -f 02-deployment.yaml
- kubectl apply -f 03-service.yaml 
- kubectl autoscale deployment php-apache --cpu-percent=50 --min=1 --max=10
- kubectl get hpa
# Abrir um outro terminal
- watch kubectl get hpa

# Abrir um outro terminal
- watch kubectl get deployment php-apache

# Abrir um outro terminal
- watch kubectl get po

# Abrir um outro terminal
- watch kubectl top pod

# Executar este comando para gerar a cargar
- kubectl run -i --tty load-generator --rm --image=busybox --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://php-apache; done"
