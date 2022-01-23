https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/

- kubectl apply -f pod.yaml
- kubectl get po
- kubectl get po --show-labels
- kubectl get po -o wide
- kubectl get po -o wide -l name=nginx-pod
- kubectl describe pod nginx-pod
- kubectl logs -f nginx-pod
- kubectl port-forward nginx-pod 8080:80