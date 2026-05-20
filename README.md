# 🔐 Secure Multi-Region Infrastructure Automation with HashiCorp Vault & Terraform on Azure

![Azure](https://img.shields.io/badge/Azure-Cloud-0078D4?logo=microsoftazure&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-IaC-7B42BC?logo=terraform&logoColor=white)
![Vault](https://img.shields.io/badge/Vault-Secrets-000000?logo=vault&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-Automation-EE0000?logo=ansible&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-System%20Administration-FCC624?logo=linux&logoColor=black)
![Azure Monitor](https://img.shields.io/badge/Azure-Monitoring-00BCF2?logo=microsoftazure&logoColor=white)

Enterprise-grade Azure infrastructure automation platform implementing Infrastructure as Code (IaC), Multi-Region Deployment, Disaster Recovery Architecture, HashiCorp Vault Secret Management, Runtime Secret Retrieval, Remote Backend State Management, Monitoring, and Enterprise Cloud Automation.

---

# 📌 Project Overview

Enterprise environments often face challenges like:

❌ Manual infrastructure provisioning

❌ Infrastructure drift

❌ Secret exposure risk

❌ Lack of disaster recovery planning

❌ Configuration inconsistency

❌ Scaling limitations

❌ Manual server management

This project was designed to solve these problems using Azure enterprise cloud engineering practices.

Goal:

✅ Multi-Region Infrastructure

✅ Infrastructure as Code

✅ Secret Management

✅ Dynamic Credentials

✅ Runtime Secret Retrieval

✅ Remote Backend

✅ Monitoring

✅ Configuration Automation

✅ Enterprise Scalability

---

# 🏗 Enterprise Architecture

![Architecture](images/project-architecture-black.png)

Flow:

Terraform

↓

Azure Infrastructure Provisioning

↓

Primary Region Deployment

↓

Secondary DR Region

↓

Remote Backend State Management

↓

Vault Secret Engine

↓

Vault Dynamic Credentials

↓

Runtime Secret Retrieval

↓

Ansible Configuration

↓

Docker + Nginx Automation

↓

Azure Monitoring

↓

VM Scale Set

↓

Load Balancer

---

# ⚙ Technology Stack

| Technology | Purpose |
|------------|----------|
| Azure | Cloud Platform |
| Terraform | Infrastructure Provisioning |
| Vault | Secret Management |
| Ansible | Configuration Management |
| Docker | Container Runtime |
| Nginx | Web Layer |
| Azure VMSS | Auto Scaling |
| Azure Load Balancer | Traffic Distribution |
| Azure Blob Storage | Remote Backend |
| Log Analytics | Monitoring |
| Linux | Server Administration |

---

# 📂 Repository Structure

```text
secure-multi-region-infrastructure-automation/

├── terraform/

├── modules/

│   ├── network/

│   ├── compute/

│   ├── security/

│   └── scaling/

├── ansible/

├── vault/

├── images/

└── README.md
```

---

# 🚀 Implementation Journey

## Phase 1 — Infrastructure Provisioning

### What I Built

Created:

- Azure Resource Groups

- Virtual Networks

- Network Security Groups

- Virtual Machines

- Backend Storage

### Why

Manual provisioning creates inconsistency.

Terraform automation ensures repeatable infrastructure deployment.

### Problem Faced

Terraform local state collaboration issue.

### Root Cause

Local state file risk.

Infrastructure drift.

### Solution

Azure Blob Storage Remote Backend.

### Outcome

Centralized infrastructure state.

Proof:

![Terraform](images/terraform-init-success.png)

![RG](images/resource-groups-created.png)

![Primary](images/primary-resource-group-resources.png)

![Secondary](images/secondary-resource-group-resources.png)

![VM](images/virtual-machines-overview.png)

---

## Phase 2 — Network Architecture

### Problem

Single subnet architecture enterprise security standard follow nahi karti.

### Solution

Implemented:

- Public Subnets

- Private Subnets

- NSG Isolation

### Outcome

Secure network segmentation.

Proof:

![Network](images/virtual-networks-overview.png)

![NSG](images/network-security-groups.png)

![Primary](images/primary-vnet-subnets.png)

![Secondary](images/secondary-vnet-subnets.png)

---

## Phase 3 — Remote Backend State Management

### Problem

Terraform local backend collaboration risk create karta hai.

### Root Cause

State conflicts.

Infrastructure drift.

### Solution

Azure Blob Storage Backend.

### Outcome

Enterprise backend management.

Proof:

![Storage](images/storage-account-overview.png)

![Blob](images/blob-storage-statefile.png)

![Backend](images/terraform-remote-backend-proof.png)

---

## Phase 4 — Monitoring

### Problem

Infrastructure visibility missing.

### Solution

Azure Log Analytics.

### Outcome

Centralized monitoring.

Proof:

![Monitoring](images/log-analytics-workspace.png)

---

## Phase 5 — HashiCorp Vault Integration

### Problem

Secrets hardcoding security risk create karta hai.

### Implemented

- Vault KV Secrets

- Dynamic Credentials

- Runtime API Integration

### Problem Faced

Vault database validation failed.

### Root Cause

PostgreSQL localhost binding.

### Solution

listen_addresses='*'

pg_hba.conf update

### Outcome

Dynamic secret rotation operational.

Proof:

![Vault](images/vault-secret-proof.png)

![Dynamic](images/vault-dynamic-credentials.png)

---

## Phase 6 — Runtime Vault API Integration

### Problem

Application runtime secret pull failed.

### Root Cause

hvac package unavailable.

### Solution

Python Virtual Environment.

Installed:

- python3-venv

- hvac

### Outcome

Runtime secret retrieval operational.

---

## Phase 7 — Terraform Module Migration

### Problem

Direct resource blocks scalable nahi hote.

### Solution

Terraform modules implementation.

Created:

- Network Module

- Compute Module

- Security Module

- Scaling Module

### Outcome

Reusable infrastructure.

Proof:

![Terraform State](images/terraform-state-list.png)

![Module](images/terraform-module-migration-proof.png)

---

## Phase 8 — Configuration Automation

### Problem

Manual package installation operational overhead create karta hai.

### Solution

Ansible Automation.

Automated:

- Docker Installation

- Nginx Installation

- Linux Updates

### Problem Faced

SSH automation failed.

### Root Cause

sshpass unavailable.

### Solution

Installed sshpass.

### Outcome

Automated configuration operational.

Proof:

![Ansible](images/ansible-configuration-proof.png)

---

## Phase 9 — Enterprise Scaling

### Problem

Single VM architecture scalable nahi.

### Solution

Implemented:

- VM Scale Set

- Load Balancer

### Outcome

Scalable infrastructure architecture.

Proof:

![VMSS](images/vmss-proof.png)

![LB](images/load-balancer-proof.png)

---

# ⚠ Engineering Challenges Solved

### Challenge 01

Terraform backend conflict.

Solution:

Azure Remote Backend.

---

### Challenge 02

Vault DB validation failure.

Solution:

PostgreSQL listener configuration.

---

### Challenge 03

SSH automation failed.

Solution:

sshpass installation.

---

### Challenge 04

Runtime API integration failed.

Solution:

Python Virtual Environment.

---

# 📈 Platform Capabilities

✅ Infrastructure as Code

✅ Multi Region Deployment

✅ Disaster Recovery

✅ Dynamic Credentials

✅ Runtime Secret Pull

✅ Monitoring

✅ VM Scale Set

✅ Load Balancer

✅ Remote Backend

✅ Configuration Automation

---

# 🧠 Skills Demonstrated

- Azure Cloud

- Terraform

- HashiCorp Vault

- Linux Administration

- Infrastructure Automation

- Monitoring

- Disaster Recovery

- Secret Management

- Networking

- DevOps Automation

- Cloud Operations

---

# 📈 Final Outcome

Successfully designed and implemented a secure enterprise-grade Azure infrastructure automation platform supporting disaster recovery capability, secret security, scalable infrastructure design, monitoring visibility, and operational automation.

---

# 👨‍💻 Author

Amit Kumar

Cloud Engineer

Azure | Terraform | Vault | DevOps | Automation
