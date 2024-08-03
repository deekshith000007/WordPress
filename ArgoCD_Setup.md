Setup Argocd on microk8s 

1.Installing Argo CD in Kubernetes

```sh 
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/core-install.yaml
```

2. Exposing the Argo CD Service
```sh 
kubectl get svc -n argocd
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
```
3. Creating a Tunnel to Access the Argo CD Server 
```sh 
kubectl get svc argocd-server -n argocd
```
4. Accessing Argo CD Server via LoadBalancer
```
Copy the LoadBalancer IP or URL from the argocd-server service : kubectl get svc argocd-server -n argocd
Paste the LoadBalancer IP or URL into your web browser to access the Argo CD server.
```
6. Getting the Password and Loggining into ArgoCD
```
Get the list of secrets in the argocd namespace
kubectl get secret -n argocd
```
Edit the argocd-initial-admin-secret to retrieve the admin password
```
kubectl edit secret argocd-initial-admin-secret -n argocd
```
Decode the password using base64
```
echo <password> | base64 --decode
```
