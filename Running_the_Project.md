 1. Open ArgoCD

- Create a New Application

- App Name: Wordpress
- Project Name: default
- Sync Policy: Automatic
- Repository URL: https://github.com/deekshith000007/WordPress.git
- Revision: HEAD
- Path: WordPress/WordPress
- Cluster URL: https://kubernetes.default.svc
- Namespace: default

- Create the Application

 2. Open Kubectl Terminal

- kubectl get pods
- kubectl get svc

 3. Access WordPress

- Copy the LoadBalancer URL of the WordPress service.
- Paste it into your browser to access the WordPress application.

 Additional Information
- Ensure your Kubernetes cluster is properly configured and running.
- ArgoCD should be installed and accessible.
- The GitHub repository should have the correct structure and files for WordPress deployment.
