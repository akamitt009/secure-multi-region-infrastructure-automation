# 🔐 Secure Multi-Region Infrastructure Automation with HashiCorp Vault & Terraform on Azure

![Azure](https://img.shields.io/badge/Azure-Cloud-0078D4?logo=microsoftazure&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-IaC-7B42BC?logo=terraform&logoColor=white)
![Vault](https://img.shields.io/badge/Vault-Secrets-000000?logo=vault&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-Automation-EE0000?logo=ansible&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-System%20Administration-FCC624?logo=linux&logoColor=black)
![Azure Monitor](https://img.shields.io/badge/Azure-Monitoring-00BCF2?logo=microsoftazure&logoColor=white)

Enterprise-grade Azure Infrastructure Automation Platform implementing:

- Infrastructure as Code (IaC)
- Multi-Region Deployment
- Disaster Recovery
- HashiCorp Vault Integration
- Runtime Secret Retrieval
- Remote Backend State Management
- Configuration Automation
- Monitoring & Observability
- VM Scale Set
- Load Balancer
- Enterprise Cloud Automation

---

# 📌 Project Overview

Enterprise cloud environments often struggle with:

❌ Manual infrastructure provisioning

❌ Infrastructure drift

❌ Secret exposure risk

❌ Configuration inconsistency

❌ Scaling limitations

❌ Disaster recovery gaps

❌ Manual operational management

This project solves those challenges using enterprise Azure cloud engineering practices.

---

# 🎯 Objectives

✅ Multi-Region Infrastructure

✅ Infrastructure as Code

✅ Disaster Recovery

✅ Secret Management

✅ Dynamic Credentials

✅ Runtime Secret Retrieval

✅ Monitoring

✅ Enterprise Scalability

✅ Configuration Automation

---

# 🛠 Prerequisites

Before deploying infrastructure ensure dependencies are installed.

| Requirement | Version |
|-------------|----------|
| Terraform | v1.5+ |
| Azure CLI | Latest |
| Azure Subscription | Required |
| Docker | Latest |
| Python | 3.10+ |
| Vault | Installed |
| Ansible | Installed |

Authenticate Azure:

```bash
az login
```

Verify Terraform:

```bash
terraform version
```

Verify Azure CLI:

```bash
az --version
```

Verify Vault:

```bash
vault version
```

---

# 🏗 Enterprise Architecture

```mermaid
graph TD

User[Traffic Manager / End User]

Hub1[East US Hub VNet]

Hub2[West Europe Hub VNet]

Spoke1[Primary Application Network]

Spoke2[DR Application Network]

Terraform[Terraform Infrastructure]

Vault[HashiCorp Vault]

Backend[Azure Blob Remote Backend]

VMSS[Azure VM Scale Set]

LB[Azure Load Balancer]

Monitor[Azure Monitor]

User -->|Primary Route| Hub1

User -->|Failover Route| Hub2

Terraform --> Hub1

Terraform --> Hub2

Terraform --> Backend

Hub1 --> Vault

Hub1 --> VMSS

VMSS --> LB

Hub1 --> Monitor

Hub1 --> Spoke1

Hub2 --> Spoke2

Hub1 <-->|Global VNet Peering| Hub2
```

---

# ⚙ Technology Stack

| Technology | Purpose |
|------------|----------|
| Azure | Cloud Platform |
| Terraform | Infrastructure Provisioning |
| Vault | Secret Management |
| Ansible | Configuration Automation |
| Docker | Container Runtime |
| Azure Blob Storage | Remote Backend |
| VM Scale Set | Auto Scaling |
| Azure Load Balancer | Traffic Distribution |
| Azure Monitor | Monitoring |
| Linux | Server Administration |

---

# ⚙ Configuration Variables

Modify deployment behavior using:

terraform.tfvars

| Variable | Description |
|-----------|-------------|
| primary_region | Primary deployment region |
| secondary_region | DR deployment region |
| hub_prefix | Hub CIDR |
| spoke_prefix | Spoke CIDR |
| vm_size | Compute SKU |
| environment | Environment Name |

Example:

```hcl
primary_region="East US"

secondary_region="West Europe"

hub_prefix="10.0.0.0/16"

environment="prod"

vm_size="Standard_B2ms"
```

---

# 📂 Repository Structure

```text

secure-multi-region-infrastructure-automation/

├── terraform/

├── modules/

│ ├── network/

│ ├── compute/

│ ├── security/

│ └── scaling/

├── ansible/

├── vault/

├── images/

└── README.md

```

---

# 🚀 Deployment Steps

Initialize:

```bash
terraform init
```

Validate:

```bash
terraform validate
```

Generate plan:

```bash
terraform plan
```

Deploy:

```bash
terraform apply
```

Destroy:

```bash
terraform destroy
```

---

# 🚀 Implementation Journey

## Phase 1 — Infrastructure Provisioning

### Solution

Terraform Automation.

### Proof

![Terraform](images/terraform-init-success.PNG)

![Resource Groups](images/resource-groups-created.PNG)

![Primary](images/primary-resource-group-resources.PNG)

![Secondary](images/secondary-resource-group-resources.PNG)

![VM](images/virtual-machines-overview.PNG)

---

## Phase 2 — Network Architecture

### Implemented

- Public Subnets
- Private Subnets
- NSG Isolation

### Proof

![Network](images/virtual-networks-overview.PNG)

![NSG](images/network-security-groups.PNG)

![Primary](images/primary-vnet-subnets.PNG)

![Secondary](images/secondary-vnet-subnets.PNG)

---

## Phase 3 — Remote Backend State Management

### Solution

Azure Blob Storage Remote Backend.

### Proof

![Storage](images/storage-account-overview.PNG)

![Blob](images/blob-storage-statefile.PNG)

![Backend](images/terraform-remote-backend-proof.PNG)

---

## Phase 4 — Monitoring

### Solution

Azure Log Analytics.

### Proof

![Monitoring](images/log-analytics-workspace.PNG)

---

## Phase 5 — HashiCorp Vault Integration

### Implemented

- Vault KV Secrets
- Dynamic Credentials
- Runtime Secret Retrieval

### Proof

![Vault](images/vault-secret-proof.png)

![Dynamic](images/vault-dynamic-credentials.PNG)

---

## Phase 6 — Runtime Secret Retrieval

### Solution

Python Virtual Environment + hvac

Runtime secret retrieval operational.

---

## Phase 7 — Terraform Module Migration

### Modules

- Network
- Compute
- Security
- Scaling

### Proof

![Terraform State](images/terraform-state-list.PNG)

![Modules](images/terraform-module-migration-proof.PNG)

---

## Phase 8 — Configuration Automation

### Automated

- Docker Installation
- Nginx Installation
- Linux Updates

### Proof

![Ansible](images/ansible-configuration-proof.PNG)

---

## Phase 9 — Enterprise Scaling

### Implemented

- VM Scale Set
- Load Balancer

### Proof

![VMSS](images/vmss-proof.PNG)

![Load Balancer](images/load-balancer-proof.PNG)

---

# 📈 Platform Capabilities

✅ Infrastructure as Code

✅ Disaster Recovery

✅ Multi Region Deployment

✅ Dynamic Credentials

✅ Runtime Secret Retrieval

✅ VM Scale Set

✅ Remote Backend

✅ Monitoring

✅ Configuration Automation

---

# 🧠 Skills Demonstrated

Azure Cloud

Terraform

HashiCorp Vault

Infrastructure Automation

Cloud Operations

Monitoring

Networking

Disaster Recovery

Linux Administration

DevOps Automation

Configuration Management

---

# 📈 Final Outcome

Successfully designed and implemented a secure enterprise-grade Azure Infrastructure Automation Platform supporting disaster recovery capability, infrastructure scalability, runtime secret retrieval, monitoring visibility and operational automation.

---

# 👨‍💻 Author

### Amit Kumar

Cloud Engineer

Azure | Terraform | Vault | DevOps | Automation
