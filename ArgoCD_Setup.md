##setup argocd on microk8s 

argocd steps:
1.

```sh 
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/core-install.yaml
```

2. Expose the service
```sh 
kubectl get svc -n argocd
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
```
3.Tunnelining use 
```sh 
kubectl get svc argocd-server -n argocd
```
4. Copy loadbalancer  paste on the browser

5. Getting the Password and Loggining into ArgoCD
```
kubectl get secret -n argocd
kubectl edit secret argocd-initial-admin-secret -n argocd
echo M2tRVjhNczFjQ0g2VlZYSQ== | base64 --decode 
```
