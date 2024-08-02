 Open ArgoCD

 1. Create a New Application
```
  1. App Name: Wordpress
  2. Project Name: default
  3. Sync Policy: Automatic
  4. Repository URL: https://github.com/deekshith000007/WordPress.git
  5. Revision: HEAD
  6. Path: WordPress/WordPress
  7. Cluster URL: https://kubernetes.default.svc
  8. Namespace: default
  9. Create the Application
```


 2. Open Kubectl Terminal
```
   kubectl get pods
   kubectl get svc
```

 3. Access WordPress
```
   Copy the LoadBalancer URL of the WordPress service.
   Paste it into your browser to access the WordPress application.
```
```
 Additional Information
- Ensure your Kubernetes cluster is properly configured and running.
- ArgoCD should be installed and accessible.
- The GitHub repository should have the correct structure and files for WordPress deployment.
```
