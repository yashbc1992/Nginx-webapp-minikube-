# Simple Helm Chart for Nginx Web App

This is a simple Helm chart to deploy a basic Nginx web server in Kubernetes using Minikube.

## Prerequisites

- Minikube
- Helm 3
- kubectl

## Deploying the App

Run the following command to install the app on [Minikube:]
```bash
./helm-install.sh


####Basic Commands####

# Start a cluster----------------minikube start

# Check status-----------------minikube status

# Open the Kubernetes dashboard-------minikube dashboard

# Stop the cluster-----------------minikube stop

# Delete the cluster---------------minikube delete

#minikube Tunnel---------------Expose LoadBalancer services

################Steps to Install and Run Minikube on EC2#################
1. Launch an EC2 Instance
------------------------------------
Use an Ubuntu-based AMI (e.g., Ubuntu 22.04).
Instance type: At least t3.medium (2 vCPUs, 4 GB RAM) recommended.
Enable inbound ports: SSH (22), Kubernetes API (default 8443), and dashboard (optional 30000–32767).

2. Install Prerequisites
----------------------------------------
SSH into your EC2 instance and run:

3. Install kubectl
4. Install Minikube
5.Start Minikube using Docker driver
6.Access the Dashboard 
7.Expose the Minikube dashboard over a public port (e.g., using SSH tunneling or minikube tunnel)..Then access the printed URL in your browser. You may need to update your security group to allow the relevant port.


