# 🚀 Azure Virtual Machine Scale Set (VMSS) Deployment with Autoscaling

## 📌 Project Summary

In this lab, I deployed and configured an **Azure Virtual Machine Scale
Set (VMSS)** using the Azure Portal.

A VM Scale Set allows you to deploy and manage a group of identical
virtual machines that can automatically scale in or out based on demand.

This project demonstrates real-world cloud administration skills
including autoscaling configuration, disk provisioning, networking
setup, and upgrade governance.

------------------------------------------------------------------------

## 🏗️ Environment Details

-   **Resource Group:** `ProdRG`
-   **VM Scale Set Name:** `vmss01`
-   **Region:** East US
-   **Availability Zone:** Zone 1
-   **Image:** Windows Server 2019 Datacenter -- x64 Gen2
-   **VM Size:** Standard_D2s_v3 (2 vCPU, 8GB RAM)
-   **Upgrade Mode:** Manual
-   **Load Balancer:** None
-   **Autoscaling:** Enabled (CPU-based)

------------------------------------------------------------------------

## 🔧 Key Configurations

### 🔐 Security

-   Security Type: **Standard**

------------------------------------------------------------------------

### 📈 Autoscaling Configuration

Configured dynamic scaling based on CPU utilization:

**Instance Limits** - Initial: 1 - Minimum: 1 - Maximum: 3

**Scale-Out Rule** - Trigger: CPU \> 75% - Action: Add 1 instance -
Evaluation period: 10 minutes

**Scale-In Rule** - Trigger: CPU \< 25% - Action: Remove 1 instance

**Scale-In Policy** - Default: Balance across zones, delete highest
instance ID

------------------------------------------------------------------------

### 💻 Virtual Machine Configuration

-   Image: Windows Server 2019
-   Architecture: x64
-   Size: Standard_D2s_v3
-   Administrator account configured with secure credentials

------------------------------------------------------------------------

### 💽 Storage Configuration

**OS Disk** - 127 GiB - Premium SSD (LRS) - Platform-managed key

**Data Disk** - Name: `vmss01_DataDisk_0` - Size: 8 GiB - Performance
Tier: P10 - Storage Type: Premium SSD (LRS)

------------------------------------------------------------------------

### 🌐 Networking Configuration

-   Virtual Network: `ProdRG-vnet`
-   Subnet: `default (10.4.0.0/20)`
-   Network Interface: `ProdRG-vnet-nic01`
-   Load Balancing: None

------------------------------------------------------------------------

### 🛠️ Management & Governance

-   Upgrade Mode: **Manual**
-   Boot Diagnostics: Enabled
-   Microsoft Defender for Cloud: Active (Plan P2)
-   Automatic OS Upgrades: Disabled

------------------------------------------------------------------------

### ❤️ Health Settings

-   Application health monitoring: Disabled
-   Automatic repairs: Disabled

------------------------------------------------------------------------

## ✅ Deployment Validation

Deployment completed successfully.

Verified: - VM instances provisioned correctly - Autoscale rules
configured - Disk attached - Networking assigned - Management policy
applied

------------------------------------------------------------------------

## 📊 What This Project Demonstrates

✔ Azure VM Scale Set deployment from scratch\
✔ CPU-based autoscaling configuration\
✔ Instance boundary control (min/max planning)\
✔ Scale-in policy configuration\
✔ Premium SSD performance tier selection\
✔ Virtual network integration\
✔ Upgrade governance strategy\
✔ Post-deployment validation

------------------------------------------------------------------------

## 🧠 Key Takeaways

-   Autoscaling improves performance and cost efficiency.
-   Instance limits prevent runaway resource consumption.
-   Upgrade policies are critical for production stability.
-   Disk performance tiers directly impact throughput and IOPS.
-   VM Scale Sets simplify scaling identical workloads.

------------------------------------------------------------------------

## 🔮 Future Enhancements

-   Add Azure Load Balancer with health probes
-   Enable application health monitoring
-   Configure automatic repair policies
-   Integrate Log Analytics for monitoring
-   Simulate load to validate scaling behavior

------------------------------------------------------------------------

## 📌 Final Reflection

This lab strengthened my understanding of scalable cloud infrastructure
design in Azure.

Deploying a VM Scale Set required planning scaling thresholds, storage
performance, upgrade policies, and networking configuration --- all
essential responsibilities of a Cloud Administrator.
