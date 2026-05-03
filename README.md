<div align="center">

# Ekwebelem Amarachi Janefrancis
### Cloud & DevOps Engineer

*I turn applications into production systems — automated, secure, and built to survive.*
</div>

<div align="center">
  <img width="736" height="414" alt="Image" src="https://github.com/user-attachments/assets/f81ca817-5931-4718-bf38-6fa4f3a07b60" />
</div>

---
---

## What I Do

I design and deploy cloud infrastructure that teams can trust — version-controlled, repeatable, and documented clearly enough that anyone can pick it up.

My work sits at the intersection of **infrastructure engineering**, **platform automation**, and **Kubernetes operations**. I've built end-to-end pipelines that go from a `git push` to a live production deployment with zero manual steps — on AWS, with real infrastructure decisions behind every choice.

What I care about:
- Infrastructure owned by Git, not by someone's terminal session
- Deployments that are boring because they always work
- Documentation that actually helps the next engineer

---

## Core Skills

**Cloud**
`AWS` &nbsp;·&nbsp; `Azure` &nbsp;·&nbsp; EC2 &nbsp;·&nbsp; EKS &nbsp;·&nbsp; AKS &nbsp;·&nbsp; S3 &nbsp;·&nbsp; RDS &nbsp;·&nbsp; ECR &nbsp;·&nbsp; Lambda &nbsp;·&nbsp; DynamoDB &nbsp;·&nbsp; CloudFront &nbsp;·&nbsp; Route 53 &nbsp;·&nbsp; IAM &nbsp;·&nbsp; VPC &nbsp;·&nbsp; EBS &nbsp;·&nbsp; CloudWatch &nbsp;·&nbsp; Azure Monitor

**Infrastructure as Code**
`Terraform` (modules, remote state, DynamoDB locking) &nbsp;·&nbsp; `Ansible`

**Containers & Orchestration**
`Docker` &nbsp;·&nbsp; `Kubernetes` &nbsp;·&nbsp; `kOps` &nbsp;·&nbsp; `Helm` &nbsp;·&nbsp; `ArgoCD` &nbsp;·&nbsp; `Calico CNI` &nbsp;·&nbsp; `Portainer`

**CI/CD & Automation**
`GitHub Actions` &nbsp;·&nbsp; `Jenkins` &nbsp;·&nbsp; `Bash scripting`

**Networking & Security**
`Nginx` &nbsp;·&nbsp; `HAProxy` &nbsp;·&nbsp; `Let's Encrypt / Certbot` &nbsp;·&nbsp; `IAM / RBAC` &nbsp;·&nbsp; `SSL/TLS` &nbsp;·&nbsp; `Secrets management`

**Observability**
`CloudWatch` &nbsp;·&nbsp; `Prometheus` &nbsp;·&nbsp; `Grafana` &nbsp;·&nbsp; `Datadog` &nbsp;·&nbsp; `Azure Monitor`

---

## Featured Projects

### Cloud-Native TaskApp — Self-Managed Kubernetes on AWS
`AWS` `kOps` `Terraform` `Kubernetes` `ArgoCD` `Docker` `ECR` `Flask` `React` `PostgreSQL` `Calico`

**[View Repository →](https://github.com/Cloudcrackamara/TaskApp-Project)** &nbsp;·&nbsp; **[Live App →](https://taskapp.taskbymara.online)**

A full-stack task management application deployed on a self-managed, highly available Kubernetes cluster — 3 control plane nodes and 3 worker nodes across 3 AWS Availability Zones, provisioned entirely with Terraform and kOps.

- Chose **kOps over EKS** deliberately — managing the full control plane exposes every decision that a managed service abstracts away: etcd configuration, CNI selection, node group topology
- Provisioned 48 AWS resources from a single `terraform apply` — VPC, subnets, NAT Gateways (one per AZ), IAM, ECR, Route53, S3 state backend with DynamoDB locking
- Configured **Calico CNI** for NetworkPolicy support — frontend pods cannot directly reach the database
- Deployed PostgreSQL as a StatefulSet with EBS persistent storage and `Retain` policy — deleted the pod mid-session to verify data survived
- Implemented GitOps with ArgoCD (`selfHeal: true`) — manual cluster changes are automatically reverted; Git is the only source of truth
- Zero-downtime rolling updates enforced via `maxUnavailable: 0`
- Debugged six simultaneous CrashLoopBackOff failures across all pods on first deployment — each had a different root cause

---

### 3-Tier Banking Application — Full Cloud-Native Deployment on EKS
`AWS` `EKS` `Terraform` `GitHub Actions` `ArgoCD` `Docker` `ECR` `RDS` `MySQL` `Route53` `React` `Node.js`

A production-grade banking application deployed end-to-end on AWS — infrastructure provisioned with Terraform, applications containerized with Docker, delivered via GitOps.

- Separate CI/CD pipelines for frontend and backend — each `git push` builds a Docker image, pushes to ECR, and updates the Kubernetes manifest repo with the new image tag
- GitOps with ArgoCD: the cluster always reflects what's in Git, with automatic sync and rollback support
- Nginx Ingress, Cert-Manager, and Route53 handling HTTPS traffic on a custom domain
- Resolved real production issues: CORS preflight failures, Terraform state drift from unmanaged resources, and stale CI pipeline configuration

> *Private repo — available on request*

---

### AWS 3-Tier Terraform Deployment
`Terraform` `AWS` `VPC` `RDS` `Auto Scaling`

**[View Repository →](https://github.com/Cloudcrackamara/AWS-3-Tier-Terraform-Deployment)**

Structured 3-tier AWS architecture built with Terraform modules — VPC design, auto-scaling groups, RDS, and load balancing, organized for real team use.

---



---

## Certifications

| Certification | Issuer |
|---|---|
| AWS Certified Cloud Practitioner | Amazon Web Services |
| DevOps & Cloud Security | DigitalWitch Academy |

---

## Connect

Currently open to Cloud Engineer, DevOps Engineer, and Platform Engineer roles — feel free to reach out.

[LinkedIn](https://www.linkedin.com/in/ekwebelemamarachi) &nbsp;·&nbsp; [Email](mailto:amarachi.ekwebelem0@gmail.com) &nbsp;·&nbsp; [Portfolio](https://cloudcrackamara.com)
