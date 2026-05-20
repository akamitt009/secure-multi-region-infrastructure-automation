# 🔐 Secure Multi-Region Infrastructure Automation with HashiCorp Vault & Terraform on Azure

![Azure](https://img.shields.io/badge/Azure-Cloud-0078D4?logo=microsoftazure&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-IaC-7B42BC?logo=terraform&logoColor=white)
![Vault](https://img.shields.io/badge/Vault-Secrets-000000?logo=vault&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-Automation-EE0000?logo=ansible&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-SystemAdministration-FCC624?logo=linux&logoColor=black)
![Azure Monitor](https://img.shields.io/badge/Azure-Monitoring-00BCF2)

Enterprise-grade cloud infrastructure automation platform implementing Infrastructure as Code (IaC), HashiCorp Vault secret management, dynamic credentials rotation, multi-region disaster recovery architecture, remote backend state management, scalable infrastructure, monitoring, and enterprise cloud operational practices on Microsoft Azure.

---

## 📌 Project Overview

This project demonstrates a production-style enterprise cloud infrastructure deployment ecosystem built on Microsoft Azure.

The platform automates infrastructure provisioning, runtime secret retrieval, monitoring visibility, disaster recovery planning, secure configuration management, infrastructure consistency, and enterprise cloud operations.

The implementation simulates real-world cloud engineering operations commonly used across enterprise environments.

---

## 🧑‍💼 Business Requirement

Objective:

✅ Eliminate manual infrastructure provisioning

✅ Secure secrets management

✅ Enable infrastructure consistency

✅ Multi-region disaster recovery capability

✅ Enterprise monitoring visibility

✅ Infrastructure automation

✅ Runtime secret retrieval

✅ Reduce operational effort

---

## 🏗 Enterprise Deployment Architecture

![Architecture](images/project-architecture-black.png)

Deployment Workflow:

Terraform Infrastructure Provisioning

↓

Azure Multi Region Deployment

↓

Primary Region Infrastructure

↓

Secondary DR Region

↓

Terraform Remote Backend

↓

HashiCorp Vault Secret Engine

↓

Vault Dynamic Credentials

↓

Runtime Secret Retrieval

↓

Ansible Configuration Management

↓

Docker + Nginx Automation

↓

Monitoring & Observability

---

## ⚙ Technology Stack

| Technology | Purpose |
|------------|----------|
| Azure | Cloud Platform |
| Terraform | Infrastructure Automation |
| HashiCorp Vault | Secret Management |
| Ansible | Configuration Automation |
| Docker | Container Runtime |
| Nginx | Web Layer |
| VM Scale Set | Scaling |
| Azure Load Balancer | Traffic Distribution |
| Azure Blob Storage | Remote Backend |
| Log Analytics | Monitoring |
| Linux | System Administration |

---

## 🔥 Enterprise Features

✅ Infrastructure as Code

✅ Multi Region Deployment

✅ Public + Private Subnet Architecture

✅ Terraform Modules

✅ Remote Backend State Management

✅ Dynamic Secret Rotation

✅ Runtime Secret Pull

✅ VM Scale Set

✅ Load Balancer

✅ Monitoring Stack

✅ Disaster Recovery Design

✅ Configuration Automation

---

## 📂 Repository Structure

```

secure-multi-region-infrastructure-automation/

├── terraform/

├── modules/

│ ├── network/

│ ├── compute/

│ ├── scaling/

│ └── security/

├── ansible/

├── vault/

├── images/

│ ├── terraform-init-success.png

│ ├── resource-groups-created.png

│ ├── primary-resource-group-resources.png

│ ├── secondary-resource-group-resources.png

│ ├── virtual-machines-overview.png

│ ├── virtual-networks-overview.png

│ ├── network-security-groups.png

│ ├── storage-account-overview.png

│ ├── blob-storage-statefile.png

│ ├── log-analytics-workspace.png

│ ├── vault-secret-proof.png

│ ├── terraform-state-list.png

│ ├── ansible-configuration-proof.png

│ ├── vmss-proof.png

│ ├── load-balancer-proof.png

│ ├── vault-dynamic-credentials.png

│ ├── primary-vnet-subnets.png

│ ├── secondary-vnet-subnets.png

│ ├── terraform-module-migration-proof.png

│ └── terraform-remote-backend-proof.png

└── README.md

```

---

## 🛠 Implementation Process

### 1️⃣ Infrastructure Provisioning

Created:

- Azure Resource Groups
- Virtual Networks
- Network Security Groups
- Virtual Machines
- Terraform Backend Storage

Infrastructure provisioning automated using Terraform.

Proof:

![Terraform](images/terraform-init-success.png)

![Resource Group](images/resource-groups-created.png)

![Primary](images/primary-resource-group-resources.png)

![Secondary](images/secondary-resource-group-resources.png)

---

### 2️⃣ Network Architecture Design

Problem:

Single subnet enterprise standards follow nahi karta.

Root Cause:

Flat network architecture security risk create karta hai.

Solution:

Implemented:

- Public Subnets
- Private Subnets
- Network Isolation

Outcome:

Enterprise network segmentation achieved.

Proof:

![VNET](images/virtual-networks-overview.png)

![NSG](images/network-security-groups.png)

![Primary](images/primary-vnet-subnets.png)

![Secondary](images/secondary-vnet-subnets.png)

---

### 3️⃣ Remote Backend State Management

Problem:

Terraform local state collaboration risk create karta hai.

Root Cause:

State conflicts.

Infrastructure drift.

Solution:

Azure Blob Storage Remote Backend.

Outcome:

Enterprise-grade state management.

Proof:

![Storage](images/storage-account-overview.png)

![Blob](images/blob-storage-statefile.png)

![Backend](images/terraform-remote-backend-proof.png)

---

### 4️⃣ HashiCorp Vault Integration

Problem:

Secrets hardcoding security risk create karta hai.

Solution:

Implemented:

- Vault KV Secret Engine
- Dynamic Credentials
- Runtime Secret Retrieval

Problem Faced:

Database connection validation failed.

Root Cause:

PostgreSQL localhost binding.

Solution:

listen_addresses='*'

Outcome:

Dynamic credentials operational.

Proof:

![Vault](images/vault-secret-proof.png)

![Dynamic Credentials](images/vault-dynamic-credentials.png)

---

### 5️⃣ Runtime Vault API Integration

Problem:

Application Vault runtime connection failed.

Root Cause:

hvac dependency unavailable.

Solution:

Python Virtual Environment.

Installed:

- python3-venv
- hvac

Outcome:

Application runtime secret pull operational.

---

### 6️⃣ Terraform Module Migration

Problem:

Direct resource blocks scalability limitation.

Solution:

Terraform modules implementation.

Outcome:

Reusable infrastructure components.

Proof:

![Module](images/terraform-module-migration-proof.png)

![State](images/terraform-state-list.png)

---

### 7️⃣ Configuration Management Automation

Problem:

Manual server configuration operational overhead create karta hai.

Solution:

Ansible Automation.

Automated:

- Docker Installation
- Nginx Installation
- Linux Updates

Problem Faced:

SSH authentication automation failed.

Root Cause:

sshpass missing.

Solution:

Installed sshpass.

Outcome:

Automated server provisioning.

Proof:

![Ansible](images/ansible-configuration-proof.png)

---

### 8️⃣ Enterprise Scaling Layer

Problem:

Single VM architecture scalability limitation.

Solution:

Implemented:

- VM Scale Set
- Load Balancer

Outcome:

Scalable infrastructure achieved.

Proof:

![VMSS](images/vmss-proof.png)

![LB](images/load-balancer-proof.png)

---

## ⚠ Engineering Challenges Solved

### Challenge 01

Problem:

Terraform backend collaboration issue.

Solution:

Azure Blob Remote Backend.

Outcome:

State consistency improved.

---

### Challenge 02

Problem:

Vault database validation failed.

Root Cause:

PostgreSQL listener configuration.

Solution:

listen_addresses='*'

Outcome:

Dynamic credentials operational.

---

### Challenge 03

Problem:

SSH automation failed.

Root Cause:

Missing sshpass.

Solution:

Installed sshpass.

Outcome:

Automation operational.

---

### Challenge 04

Problem:

Vault runtime integration failed.

Root Cause:

Missing hvac dependency.

Solution:

Python virtual environment.

Outcome:

Runtime secret retrieval operational.

---

## 📈 Platform Capabilities

| Capability | Status |
|------------|---------|
| Terraform IaC | ✅ |
| Multi Region DR | ✅ |
| Runtime Secret Pull | ✅ |
| Dynamic Credentials | ✅ |
| VM Scale Set | ✅ |
| Load Balancer | ✅ |
| Monitoring | ✅ |
| Infrastructure Automation | ✅ |
| Configuration Automation | ✅ |

---

## 🧠 Skills Demonstrated

Azure Cloud

Terraform

HashiCorp Vault

Infrastructure Automation

Disaster Recovery

Secret Management

Monitoring

Linux Administration

Ansible

Networking

Cloud Security

Cloud Operations

Troubleshooting

---

## 📈 Final Outcome

Successfully designed and implemented an enterprise-grade multi-region Azure infrastructure platform supporting automation, monitoring, secrets security, disaster recovery capability, remote backend state management, and cloud operational practices.

---

## 👨‍💻 Author

Amit Kumar

Cloud Infrastructure Engineer

Azure | Terraform | Vault | DevOps | Automation
