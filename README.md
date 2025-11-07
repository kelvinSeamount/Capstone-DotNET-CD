![alt text](<FLow Diagaram.png>)



                                Overview
This repository contains the Continuous Deployment (CD) pipeline for a .NET Note Application deployed on AWS EKS (Kubernetes). The pipeline automates the deployment process, manages SSL certificates, integrates with HashiCorp Vault for secrets management, and provides verification of successful deployments.

Deployment Flow

    Trigger CI pipeline completes successfully and updates CD repository

    Git Checkout CD pipeline pulls latest Kubernetes manifests

    Deploy Apply manifests to EKS cluster (Deployment, Service, Ingress, SSL)

    Verify Check pods, services, and ingress status

    Notify Send email notification with deployment status


                            Technology Stack


Infrastructure

    AWS EKS Managed Kubernetes cluster (mekadevops-cluster)

    Kubernetes for container orchestration

    Jenkins CD automation server running on EC2


Security & Secrets

    HashiCorp Vault Secrets management for MongoDB connection string

    Cert-Manager Automated SSL/TLS certificate management

    Let's Encrypt Free SSL certificates (Production)


Networking

    Nginx Ingress Controller External traffic routing

    Domain piroo.online & www.piroo.online 

    
