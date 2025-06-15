**🚀 DevOpsified**

End-to-end DevOps pipeline for containerized microservices with GitHub Actions, Docker, Terraform, Kubernetes, and GitOps deployment via ArgoCD.


![image](https://github.com/user-attachments/assets/3ef515ff-224e-475c-bf37-a4795b214ce0)


**📑 Table of Contents**

## About
## Technologies
## Conclusion
## Author


**📌 About**

Modern software delivery needs speed, security, and scalability. DevOpsified is a project that simulates a real-world production-grade DevOps workflow using a Go-based microservice.

This pipeline demonstrates how a single code push can trigger a complete CI/CD workflow—from code build, vulnerability scanning, image packaging, infrastructure provisioning, all the way to Kubernetes deployment using GitOps.

The project automates infrastructure using Terraform on AWS (EKS, VPC, IAM), builds and tests the Go app, pushes Docker images to ECR, and deploys the application using ArgoCD into Kubernetes. This model is aligned with industry-grade practices followed by MNCs and SRE teams for production-grade environments.


**🛠 Technologies**

Go (Golang) – Lightweight web API service
Docker – Containerization with multi-stage builds
GitHub Actions – CI pipeline: build, test, scan, push
Terraform – Infrastructure as Code (IaC) on AWS
AWS EKS – Managed Kubernetes cluster
Kubernetes – Orchestration, manifests, and Helm
ArgoCD – GitOps continuous deployment
Trivy / Clair – Security scanning
SonarQube – Code quality analysis


**✅ Conclusion**

The pipeline successfully demonstrates the Dev → CI → CD → Deploy journey using real-world tools and practices. A developer pushes code to GitHub, which automatically:
Runs tests and static checks
Builds a Docker image
Scans for vulnerabilities
Pushes to Docker registry
Deploys infra with Terraform
Deploys app via ArgoCD

This kind of pipeline reduces manual effort, improves developer confidence, and ensures that applications are shipped in a reliable and secure manner.
Companies can leverage this approach for faster release cycles, automated rollbacks, and cloud-native scalability.

**Author**

Created by Sailaja Rowthu, please feel free to contact me at shailajarowthu@gmail.com, thank you for your time!
