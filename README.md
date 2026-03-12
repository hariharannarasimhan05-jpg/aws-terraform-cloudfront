# AWS Global Content Delivery Architecture 🚀

## Overview
This project demonstrates a production-ready approach to hosting static content globally. Using **Terraform**, I deployed a secure, high-performance architecture that leverages **Amazon CloudFront** to serve content from an **Amazon S3** origin.

## 🏗️ Architecture
- **Amazon S3**: Acts as the "Origin" storage. The bucket is configured to be private, ensuring no direct public access.
- **Amazon CloudFront (CDN)**: Distributes content to 600+ Edge Locations globally for ultra-low latency.
- **Origin Access Control (OAC)**: Implements a secure handshake between CloudFront and S3. This ensures that the bucket only accepts requests coming from my specific CloudFront distribution.
- **Terraform (IaC)**: The entire stack is managed as code, allowing for repeatable and predictable deployments.

## 🛠️ Tech Stack
- **Cloud Provider**: AWS
- **Infrastructure as Code**: Terraform (HCL)
- **Security**: IAM Policies, Origin Access Control (OAC)
- **Version Control**: Git & GitHub

## 🚀 Key Features & Learning Outcomes
- **Security First**: Instead of making the S3 bucket public, I implemented **OAC**, a best-practice security measure that keeps the storage layer invisible to the public internet.
- **Performance Optimization**: Configured **CloudFront Caching** and **Invalidations** to manage how content is updated across the global network.
- **Troubleshooting**: Successfully managed the Terraform state lifecycle, including handling bucket deletion dependencies and policy propagation.

## 📂 Project Structure
- `main.tf`: Contains the provider, S3 bucket, CloudFront distribution, and OAC configuration.
- `variables.tf`: Defines input variables for security and scalability.
- `index.html`: A custom, CSS-styled landing page served at the edge.

## 📝 How to Deploy
1. Clone the repository.
2. Configure your AWS credentials (using variables to avoid hardcoding secrets).
3. Run `terraform init` to initialize the providers.
4. Run `terraform apply` to deploy the global infrastructure.

---
**Author:** Hariharan  
*Transitioning from Data Center Operations to Cloud Engineering | AWS SAA-C03 Candidate*
