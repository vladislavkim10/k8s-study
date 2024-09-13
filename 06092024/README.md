# k8s-study-exam-06/09/2024
Tasks:

1. **Create a namespace and service account
 - Configure roles, rolebindings, and permissions (get, list, create, delete for pod and deployment resources).
 - Create a config file and a Dockerfile with the Kubernetes CLI and config.
 - Deploy a pod in Kubernetes from the Dockerfile, test pod commands.


2. **Create Nginx deployment:**
   - Deploy Nginx with two replicas.

3. **Create Redis pods:**
   - Deploy two Redis pods.
   - Check readiness using TCP socket type (Redis port 6379).
   - Deploy to a specific node with affinity rules.
 
4. **ConfigMap creation:**
   - Create a ConfigMap with a message `Proxima Uacademy DevOps Course`.
 
5. **Create frontend deployment:**
   - Deploy a frontend app (`visionindark/2048-react:v1`) on port 3000 with resource limits (CPU, memory).
   - Set up a liveness check with `httpGet`.

6. **Ingress for SSL:**
   - Create an ingress with SSL for the frontend service and configure it using a cluster-issuer.
 
7. **Nginx pod readiness probe:**
   - Set up an Nginx pod with a readiness probe on `/` and expose port 80.


 
8. **Another ConfigMap creation:**
   - Create a ConfigMap with key-value pairs and mount it as a volume.
 
9. **Flask app deployment:**
   - Deploy a Flask app (`nvrbckdown/something:v1`) on port 80 with environment variables and affinity rules.
   - Check the status with a liveness probe using TCP socket.

10. **List nodes in JSON format:**
    - Get the list of nodes and store the output in a file.


11. **Expose deployments:**
    - Expose the earlier created deployments.
 
12. **Ingress manifest creation:**
    - Create an ingress for the Flask app on `/config` and the frontend app on `/`.
 
13. **DaemonSet creation:**
    - Create a DaemonSet using the Nginx image, ensure pods are scheduled on each node.



14. **Secret creation:**
    - Create a secret for environment variables (`ENVIRONMENT`, `LOG_LEVEL`, etc.) and use it in a new deployment.

15. **CronJob creation:**
    - Create a CronJob with a busybox image that echoes the pod IP every 3 minutes.
 
16. **RBAC creation:**
    - Create RBAC for listing pods, cronjobs, and jobs, with permission to get, list, and check.

18. **Nginx deployment with NetworkPolicy:**
    - Create an Nginx deployment with two replicas, expose it via a ClusterIP service on port 80.
    - Create a NetworkPolicy that allows access only from a pod with the label `access: granted` and IP `192.168.10.10`.

19. **Redis pod with persistent storage:**
    - Create a Redis pod using the `redis:alpine` image with an emptyDir volume and mount it at `/data/redis`.
