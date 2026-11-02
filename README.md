# Multi-Cloud Network Deployment & Health Monitoring (GCP & OCI)

A foundational Infrastructure as Code (IaC) project demonstrating isolated network configuration, virtual compute instance provisioning, and automated endpoint health checking across Google Cloud Platform (GCP) and Oracle Cloud Infrastructure (OCI).

## Architecture Overview
- **VPC / VCN Isolation:** Provisioned custom Virtual Private Cloud (VPC) with tailored subnets and strict firewall egress/ingress policies.
- **Compute Instance:** Provisioned a light web server running Nginx via custom startup scripts.
- **Network Security:** Implemented principle of least privilege using security tags and targeted CIDR rules (blocking default ingress except SSH/HTTP).
- **Monitoring Automation:** Python automation script for verifying node reachability and continuous uptime status.

## Technologies Used
- **Cloud Infrastructure:** Google Cloud Platform (GCP), Oracle Cloud Infrastructure (OCI)
- **Infrastructure as Code:** Terraform
- **Automation / Scripting:** Python 3, `requests`
- **Networking:** Custom Subnets, Security Rules, Ingress/Egress Rules, CIDR

## Setup & Deployment

### 1. Provision Infrastructure with Terraform
Navigate to the terraform directory and initialize the environment:
```bash
cd terraform
terraform init
terraform plan
terraform apply
