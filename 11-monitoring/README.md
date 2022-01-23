https://codeberg.org/hjacobs/kube-ops-view
- GIT_SSL_NO_VERIFY=1 git clone https://codeberg.org/hjacobs/kube-ops-view.git
- cd kube-ops-view
- kubectl apply -k deploy 
- kubectl port-forward service/kube-ops-view 8080:80
- http://localhost:8080/


https://k9scli.io/topics/install/
Instalação no Ubuntu -> docker run --rm -it -v ~/.kube/config:/root/.kube/config quay.io/derailed/k9s

https://k8slens.dev/desktop.html

VS Code Kubernetes Extension