# Nginx-webapp-minikube-

Running a  Helm chart using Minikube, which is perfect for local Kubernetes development.
________________________________________
✅ Step-by-Step: Deploying with Minikube
________________________________________
🔹 1. Install Prerequisites
•	Minikube: https://minikube.sigs.k8s.io/docs/start/
•	Helm: https://helm.sh/docs/intro/install/
•	kubectl: https://kubernetes.io/docs/tasks/tools/
________________________________________
🔹 2. Start Minikube
minikube start
This spins up a local Kubernetes cluster.
________________________________________
🔹 3. Enable Minikube Tunnel (for LoadBalancer services)
Keep this running in a separate terminal.
________________________________________
🔹 4. Unzip and Prepare the Helm Chart
Expand-Archive -Path .\nginx-chart.zip -DestinationPath .
cd .\nginx-chart
________________________________________
🔹 5. (Optional) Modify values.yaml for Minikube
Change service.type to LoadBalancer if you want to access via external IP:
yaml
CopyEdit
service:
  type: LoadBalancer
  port: 80
________________________________________
🔹 6. Deploy the Chart
helm install my-nginx .
________________________________________
🔹 7. Check Status
kubectl get svc
Then access it at: http://localhost:8080
________________________________________
🔹 8. Clean Up
helm uninstall my-nginx
minikube stop
________________________________________



