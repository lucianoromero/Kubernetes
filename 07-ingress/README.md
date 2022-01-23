# Implantação do Nginx Ingress Controller
https://kubernetes.github.io/ingress-nginx/deploy/#quick-start
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.1.0/deploy/static/provider/cloud/deploy.yaml

# Criar a entrada no arquivo hosts (c:\windows\system32\drivers\etc\hosts ou /etc/hosts):
127.0.0.1     workshop-springboot.com

# Implantação da Aplicação hello-app:1.0
- kubectl create deployment web --image=gcr.io/google-samples/hello-app:1.0
- kubectl expose deployment web --type=NodePort --port=8080
- kubectl get service web
- kubectl describe service web
- kubectl apply -f 01-ingress.yaml
- kubectl get ingress
- kubectl describe ingress example-ingress
- http://workshop-springboot.com 

# Implantação da Aplicação hello-app:2.0
- kubectl create deployment web2 --image=gcr.io/google-samples/hello-app:2.0
- kubectl expose deployment web2 --port=8080 --type=NodePort
- kubectl get service web2
- kubectl describe service web2
- kubectl apply -f 02-ingress.yaml
- kubectl get ingress
- kubectl describe ingress example-ingress
- http://workshop-springboot.com/v2

# Comandos scale
- kubectl get po -o wide
- kubectl scale deployments/web --replicas=2
- kubectl scale deployments/web2 --replicas=2
- kubectl get po -o wide
