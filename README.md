# Exploring Kubernetes Namespaces

This repository demonstrates the creation and management of Kubernetes namespaces, showcasing the isolation of resources in a Kubernetes cluster. It includes scripts and YAML configurations for setting up namespaces, deploying applications, and viewing resources in AWS.

## Files Included:
- **namespace-dev.yaml**: YAML configuration to create the development namespace.
- **namespace-prod.yaml**: YAML configuration to create the production namespace.
- **script.sh**: Bash script for setting up Minikube, Docker, and Kubernetes.
- **cluster-overview.png**: Screenshot of the Kubernetes cluster overview.
- **dev-namespaces-deployments & pods.png**: Screenshot showing deployments and pods in the development namespace.
- **ec2-server.png**: Screenshot of AWS EC2 running the Kubernetes server.
- **namespace-labels.png**: Screenshot of labels applied to namespaces.
- **prod-namespaces-deployments & pods.png**: Screenshot showing deployments and pods in the production namespace.

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/Mohan006007/exploring-kubernetes-namespaces.git
2. Navigate to the repository directory:
   ```bash
   cd exploring-kubernetes-namespaces
3. Apply namespace YAML files:
   ```bash
   kubectl apply -f namespace-dev.yaml
   kubectl apply -f namespace-prod.yaml
4. Run the Minikube setup script to configure Kubernetes and Docker:
   ```bash
   bash script.sh
5. After script execution, check the Kubernetes cluster and deployed resources:
   ```bash
   kubectl get namespaces
   kubectl get pods -n development
   kubectl get pods -n production
## Script Details:
  The script.sh performs the following actions:
  1. Installs necessary dependencies (git, docker, kubectl, minikube).
  2. Starts Docker and enables it for the EC2 user.
  3. Installs Minikube and kubectl.
  4. Initializes the Minikube cluster using minikube start.
   


   
