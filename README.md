# kubernetes-example
Repo for Kubernetes examples. 

# Deployments
- [nginx](example-deployments/example-nginx.yaml): create a deployment with one pod and a service object.
  ```bash
    kubectl create -f example-nginx.yaml            # create a deployment & service object on K8s cluster.
    kubectl get pods                                # to get the created pod.    
    kubectl get service                             # to get the created service.
    kubectl get all                                 # to get all the created objects.
    kubectl port-forward pod/<pod-name> 8080:80     # to access the created pod app.
    curl -k http://localhost:8080/                  # to access nginx default page.
  ```  
.