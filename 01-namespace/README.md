https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/
- kubectl apply -f namespace.yaml
- kubectl get namespaces
- kubectl get pods -o wide --all-namespaces
- kubectl get pods -o wide
- kubectl get pods -o wide -n workshop
- kubectl get po -o wide -n workshop --show-labels
- kubectl describe pod nginx -n workshop
- kubectl logs nginx -n workshop
- kubectl logs -f nginx -n workshop
- kubectl port-forward nginx 8080:80 -n workshop
- http://localhost:8080
 