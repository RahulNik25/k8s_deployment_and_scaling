# Task
  -  Create a Kubernetes deployment for a web application using NGINX container image.
  -  Scale the deployment to handle increased traffic by increasing the number of replicas dynamically.
  -  Implement Horizontal Pod Autoscaler (HPA) to automatically scale the deployment based on CPU utilization.

# Steps to Achieve
Deploy Metrics Server, If Not Present
- `kubectl apply -f metrics-server-components.yaml`

Deploy Application
- `kubectl apply -f nginx-app.yaml`

Deploy HPA
 - `kubectl apply -f hpa.yaml`

Execute script to simulate load and notice the application scale-out and scale-in
 - `/bin/bash simulate_load.sh "http://<service-ip/name>:<expose_port>"`