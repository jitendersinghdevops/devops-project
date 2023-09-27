# DevOps Microservice Deployment Project

## Project Overview

Welcome to our DevOps Microservice Deployment Project! Our primary objective in this endeavor is to leverage cutting-edge DevOps practices to automate and streamline the deployment process of a microservice onto a Kubernetes cluster. We are deeply committed to achieving the highest levels of operational efficiency and unwavering reliability throughout this journey.

## Key Goals

Our key goals for this project include:

- Implementing industry-leading DevOps methodologies.
- Automating the deployment process for our microservice.
- Ensuring rapid and consistent deployments.
- Adhering to best practices at every stage of the project.

## Project Details

In this repository, you will find various components, tools, and resources that are integral to our project:

- **Terraform Scripts**: Used for defining and provisioning Azure infrastructure.
- **GitHub Actions Workflows**: Implemented for continuous integration and automated testing.
- **Bash Scripts**: Developed for task automation and orchestration.
- **Dockerfiles**: Used to containerize our microservice.
- **Kubernetes Manifests**: Employed to manage microservice deployments on AKS.
- **Nginx Ingress Configuration**: Facilitating routing of traffic.
- **ArgoCD Configuration**: Enabling GitOps deployment.

## Tools Required

To successfully complete this project, you'll need the following tools and technologies:

- GitHub and GitHub Actions Pipeline
- Terraform Enterprise
- Azure CLI
- Azure Kubernetes Service (AKS)
- Docker
- Helm Charts
- YAML and JSON
- Nginx Ingress
- ArgoCD
- Reloader
- AKV2k8s (Azure Key Vault to Kubernetes)
- Bash

## Getting Started

To get started with this project, follow these steps:

### Source Code

1. Clone this repository to your local development environment.
2. Create your working branch and make commits to it following our branching strategy: 
   - Use a working branch for development.
   - The master branch is for pre-production.
   - Release tags are for production environments.

### Bash or PowerShell Scripts

1. Create a script to create a Service Principal (SPN) on Azure Cloud and set up the SPN credentials in the GitHub repository automatically.
2. Create a Terraform Cloud account, organization, and workspace to store the Terraform state.

### Terraform Code

1. Use Terraform to create the following Azure resources:
   - Azure Resource Group
   - Azure Virtual Network (VNet) with one subnet
   - AKS Cluster with two node pools (appnodepool and tools nodepool)
   - Azure Key Vault with access policies
   - Azure Container
   - Note: Create Terraform modules for the above resources and maintain consistent naming conventions for dev, preprod, and prod resources.

### GitHub Actions Pipeline

Set up a GitHub Actions pipeline to automatically create the specified resources.

### Bootstrap Cluster

Once the cluster is ready, bootstrap it with the necessary tools. These tools should be deployed to the tools node pool and include:
- ArgoCD
- Nginx Ingress
- Reloader
- AKV2k8s

### CI Pipeline

Create a Dockerfile to package and build the Docker container, then push that container to Docker Hub. You can reference existing code for this.

### Kubernetes Manifests

Create Kubernetes manifests for your microservice, ensuring they are ready to use the same Docker images built in the CI pipeline.

### Automated Deployments

Automate the deployment of microservices to Kubernetes using GitOps with ArgoCD.

## License

This project is licensed under the [MIT License](LICENSE).
