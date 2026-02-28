# 🚀 Azure Virtual Machine Scale Set (VMSS) Deployment with Autoscaling

## 📌 Lab Overview

In this lab, I deployed and configured an Azure Virtual Machine Scale
Set (VMSS) using the Azure Portal.

The goal was to: - Deploy a scalable set of virtual machines - Configure
CPU-based autoscaling - Attach Premium SSD storage - Configure
networking - Apply upgrade governance settings - Validate deployment
success

------------------------------------------------------------------------

# 🗂️ Repository Structure

azure-vmss-lab/ │ ├── README.md └── images/ ├── vmss-01.png ├──
vmss-02.png ├── ... └── vmss-39.png

------------------------------------------------------------------------

# 🏗️ Deployment Steps

## Step 1 -- Create Virtual Machine Scale Set

-   Navigate to Create a resource
-   Search for Virtual machine scale set
-   Click Create

📷 Screenshot\
images/vmss-01.png

------------------------------------------------------------------------

## Step 2 -- Configure Basic Settings

-   Resource Group: ProdRG
-   VMSS Name: vmss01
-   Region: East US
-   Availability Zone: Zone 1

📷 Screenshot\
images/vmss-02.png

------------------------------------------------------------------------

## Step 3 -- Configure Security Type

-   Security Type: Standard

📷 Screenshot\
images/vmss-03.png

------------------------------------------------------------------------

## Step 4 -- Enable Autoscaling

-   Selected Autoscaling
-   Clicked Configure

📷 Screenshot\
images/vmss-04.png

------------------------------------------------------------------------

## Step 5 -- Configure Instance Limits

-   Initial instances: 1
-   Minimum: 1
-   Maximum: 3

📷 Screenshot\
images/vmss-05.png

------------------------------------------------------------------------

## Step 6 -- Configure Scale-Out Rule

-   CPU \> 75%
-   Increase instance count by 1
-   Evaluation: 10 minutes

📷 Screenshot\
images/vmss-06.png

------------------------------------------------------------------------

## Step 7 -- Configure Scale-In Rule

-   CPU \< 25%
-   Decrease instance count by 1

📷 Screenshot\
images/vmss-07.png

------------------------------------------------------------------------

## Step 8 -- Select Scale-In Policy

-   Default (Balance across zones)

📷 Screenshot\
images/vmss-08.png

------------------------------------------------------------------------

## Step 9 -- Configure VM Image & Size

-   Windows Server 2019 Datacenter -- x64
-   VM Size: Standard_D2s_v3

📷 Screenshot\
images/vmss-09.png

------------------------------------------------------------------------

## Step 10 -- Configure Administrator Account

-   Username: vmadmin
-   Secure password configured

📷 Screenshot\
images/vmss-10.png

------------------------------------------------------------------------

## Step 11 -- Review Spot Settings

-   Spot instances not enabled

📷 Screenshot\
images/vmss-11.png

------------------------------------------------------------------------

## Step 12 -- Configure OS Disk

-   127 GiB
-   Premium SSD (LRS)

📷 Screenshot\
images/vmss-12.png

------------------------------------------------------------------------

## Step 13 -- Create & Attach Data Disk

-   Created new disk
-   Name: vmss01_DataDisk_0

📷 Screenshot\
images/vmss-13.png

------------------------------------------------------------------------

## Step 14 -- Select Disk Size & Performance Tier

-   8 GiB
-   Performance Tier: P10

📷 Screenshot\
images/vmss-14.png

------------------------------------------------------------------------

## Step 15 -- Configure Networking

-   Virtual Network: ProdRG-vnet
-   Subnet: default (10.4.0.0/20)
-   Load balancing: None

📷 Screenshot\
images/vmss-15.png

------------------------------------------------------------------------

## Step 16 -- Configure Management Settings

-   Upgrade Mode: Manual
-   Boot Diagnostics: Enabled
-   Defender for Cloud: Active

📷 Screenshot\
images/vmss-16.png

------------------------------------------------------------------------

## Step 17 -- Configure Health Settings

-   Application health monitoring: Disabled
-   Automatic repairs: Disabled

📷 Screenshot\
images/vmss-17.png

------------------------------------------------------------------------

## Step 18 -- Review Advanced Settings

-   Max spreading algorithm
-   No extensions configured

📷 Screenshot\
images/vmss-18.png

------------------------------------------------------------------------

## Step 19 -- Review + Create

-   Validation passed
-   Clicked Create

📷 Screenshot\
images/vmss-19.png

------------------------------------------------------------------------

## Step 20 -- Deployment Completed

-   Deployment succeeded
-   Navigated to resource

📷 Screenshot\
images/vmss-20.png

------------------------------------------------------------------------

# 📊 What This Lab Demonstrates

✔ Azure VM Scale Set deployment\
✔ CPU-based autoscaling configuration\
✔ Instance boundary control\
✔ Premium SSD disk provisioning\
✔ Networking configuration\
✔ Upgrade governance strategy\
✔ Deployment validation

------------------------------------------------------------------------

# 🧠 What I Learned

-   Autoscaling improves performance and cost efficiency
-   Upgrade mode selection impacts production governance
-   Premium SSD tiers affect IOPS and throughput
-   VMSS simplifies horizontal scaling
-   Instance limits prevent uncontrolled scaling

------------------------------------------------------------------------

# 🔮 Future Improvements

-   Add Load Balancer with health probes
-   Enable automatic repair policy
-   Add Log Analytics monitoring
-   Simulate load to trigger scaling events
