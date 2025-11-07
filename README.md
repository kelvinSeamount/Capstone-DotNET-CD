![alt text](<FLow Diagaram.png>)



                                Overview
This repository contains the Continuous Deployment (CD) pipeline for a .NET Note Application deployed on AWS EKS (Kubernetes). The pipeline automates the deployment process, manages SSL certificates, integrates with HashiCorp Vault for secrets management, and provides verification of successful deployments.

Deployment Flow

    Trigger CI pipeline completes successfully and updates CD repository

    Git Checkout CD pipeline pulls latest Kubernetes manifests

    Deploy: Apply manifests to EKS cluster (Deployment, Service, Ingress, SSL)