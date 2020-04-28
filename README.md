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
# Published Posts
- Pod Eviction
  - Part 1: [Please don’t evict my pod; QoS Class](https://itnext.io/please-dont-evict-my-pod-part-1-399640df3ddb?source=friends_link&sk=7fbe0c04353c59e17ba40a0bd63341c0)
  - Part 2: [Please don’t evict my pod; eviction policy](https://itnext.io/please-dont-evict-my-pod-eviction-policy-ef4c5380f5fd?source=friends_link&sk=0b60541f93cbf36c45a7e5921e852174)
  - Part 3: [Please don’t evict my pod; priority & disruption budget](https://itnext.io/please-dont-evict-my-pod-priority-disruption-budget-e099da7b93d2?source=friends_link&sk=54e8636b7c321f726c1cc04b85a7128f)
  - Part 4: [Please don’t evict my pod; tips & tricks to avoid pod eviction](https://itnext.io/please-dont-evict-my-pod-tips-tricks-to-avoid-pod-eviction-e9ed466ffda6?source=friends_link&sk=3478093e28d68de42c1ebf72fa915dbc)
- Kube Scheduler
  - [Beyond Kube-scheduler, a need for a K8s Cluster Balancer](https://itnext.io/beyond-kube-scheduler-a-need-for-a-k8s-cluster-balancer-89cdfb242e09?source=friends_link&sk=288a4f53a087fc039cff9b40dded0d79)