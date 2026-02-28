# 🚀 Azure Virtual Machine Scale Set (VMSS) Deployment with Autoscaling

## 📌 Lab Overview

In this lab, I deployed and configured an Azure Virtual Machine Scale
Set (VMSS) using the Azure Portal.

The goal was to: - Deploy a scalable set of virtual machines - Configure
CPU-based autoscaling - Attach Premium SSD storage - Configure
networking - Apply upgrade governance settings - Validate deployment
success

------------------------------------------------------------------------


# 🏗️ Deployment Steps

## Step 1 -- Create Virtual Machine Scale Set

-   Navigate to Create a resource
-   Search for Virtual machine scale set
-   Click Create


![vm1](https://github.com/user-attachments/assets/540d634e-5b58-4bb3-a770-4773a1921a0f)
![vm2](https://github.com/user-attachments/assets/341d6ede-c349-48c8-b482-202a958048a6)
![vm3](https://github.com/user-attachments/assets/014754b7-7a3d-4bf0-b5d3-eb5f98c5cf28)
![vm4](https://github.com/user-attachments/assets/bee704b2-4e12-490f-a049-f3e3a1e32c9c)
![vm5](https://github.com/user-attachments/assets/6ed16d0e-1cda-42d7-bd57-f996e7984ed7)



------------------------------------------------------------------------

## Step 2 -- Configure Basic Settings

-   Resource Group: ProdRG
-   VMSS Name: vmss01
-   Region: East US
-   Availability Zone: Zone 1

![vm6](https://github.com/user-attachments/assets/4d1f2d7b-b54a-4a18-b3e4-e06d9a6856fd)
![vm7](https://github.com/user-attachments/assets/ae294fd1-b3b6-43c5-9e92-a10a8fe2deae)
![vm8](https://github.com/user-attachments/assets/697c4e21-c074-4f43-9b41-74d3fcd0469c)
![vm9](https://github.com/user-attachments/assets/fad347ff-8073-4e62-9990-8eee28f0db9e)
![vm10](https://github.com/user-attachments/assets/56eed18e-3595-4e86-acc9-3d22f9405e4c)





------------------------------------------------------------------------

## Step 3 -- Configure Security Type

-   Security Type: Standard

![vm11](https://github.com/user-attachments/assets/6ee011e8-343b-4ff9-94c6-96dde1a6c984)


------------------------------------------------------------------------

## Step 4 -- Enable Autoscaling

-   Selected Autoscaling
-   Clicked Configure

![vm12](https://github.com/user-attachments/assets/231e8ed4-db55-45a4-b8aa-bd5fea54f982)
![vm13](https://github.com/user-attachments/assets/c53a6a7e-6301-4891-971c-8da840babd1d)


------------------------------------------------------------------------

## Step 5 -- Configure Instance Limits

-   Initial instances: 1
-   Minimum: 1
-   Maximum: 3

![vm14](https://github.com/user-attachments/assets/9143e408-8a70-4520-988b-d31c43d4ca53)
![vm15](https://github.com/user-attachments/assets/53493c84-826e-4f1a-bdd1-3c0de769272d)
![vm16](https://github.com/user-attachments/assets/a318334f-b8d0-46db-9334-0b6b8e1cad7f)


------------------------------------------------------------------------

## Step 6 -- Configure Scale-Out Rule

-   CPU \> 75%
-   Increase instance count by 1
-   Evaluation: 10 minutes

![vm16](https://github.com/user-attachments/assets/bc5a8422-5312-4f6e-97e6-c4539f0af9f8)


------------------------------------------------------------------------

## Step 7 -- Configure Scale-In Rule

-   CPU \< 25%
-   Decrease instance count by 1

![vm17](https://github.com/user-attachments/assets/328513c5-1841-488e-9fd4-90d203d8d0f8)

------------------------------------------------------------------------

## Step 8 -- Select Scale-In Policy

-   Default (Balance across zones)

![vm18](https://github.com/user-attachments/assets/ead785b1-70d8-4df6-ad41-fe02e88cc7d3)
![vm19](https://github.com/user-attachments/assets/e0b29990-5afa-4b84-a9da-5d41dae5506d)


------------------------------------------------------------------------

## Step 9 -- Configure VM Image & Size

-   Windows Server 2019 Datacenter -- x64
-   VM Size: Standard_D2s_v3

![vm20](https://github.com/user-attachments/assets/9b3eda68-db99-45df-bddd-3d09223939b9)


------------------------------------------------------------------------

## Step 10 -- Configure Administrator Account

-   Username: vmadmin
-   Secure password configured

![vm21](https://github.com/user-attachments/assets/d1c6afb9-5494-4d88-b50f-490bc3c87a76)


------------------------------------------------------------------------

## Step 11 -- Review Spot Settings

-   Spot instances not enabled

![vm22](https://github.com/user-attachments/assets/b27e5a64-669f-4243-b511-83e48cd3295f)

------------------------------------------------------------------------

## Step 12 -- Configure OS Disk

-   127 GiB
-   Premium SSD (LRS)

![vm23](https://github.com/user-attachments/assets/169e2dde-9301-4b84-9559-c4ada7e570e6)

![vm24](https://github.com/user-attachments/assets/07f701eb-c5cc-4914-b682-0c43bea651f3)


------------------------------------------------------------------------

## Step 13 -- Create & Attach Data Disk

-   Created new disk
-   Name: vmss01_DataDisk_0

![vm25](https://github.com/user-attachments/assets/d68c2022-becc-4eb8-a617-f5d1d3f588a8)


------------------------------------------------------------------------

## Step 14 -- Select Disk Size & Performance Tier

-   8 GiB
-   Performance Tier: P10

![vm26](https://github.com/user-attachments/assets/b3c1ae79-2e12-434f-8f48-502fe937cc16)
![vm27](https://github.com/user-attachments/assets/bca3322c-06bb-4d08-82ea-5ab1c11c5d0b)
![vm28](https://github.com/user-attachments/assets/c9e80707-ec6d-480e-8b0c-f864d1763832)
![vm29](https://github.com/user-attachments/assets/2b74b86e-142a-4937-a8e2-06aa774435d1)


------------------------------------------------------------------------

## Step 15 -- Configure Networking

-   Virtual Network: ProdRG-vnet
-   Subnet: default (10.4.0.0/20)
-   Load balancing: None

![vm30](https://github.com/user-attachments/assets/cdde1a8a-37b7-47d7-a2d8-388829465a48)

![vm31](https://github.com/user-attachments/assets/91d0552c-283f-4b25-beca-19e075f540d1)


------------------------------------------------------------------------

## Step 16 -- Configure Management Settings

-   Upgrade Mode: Manual
-   Boot Diagnostics: Enabled
-   Defender for Cloud: Active

![vm32](https://github.com/user-attachments/assets/a26895d2-b4dc-48c7-957e-0b07de65cf39)

![vm33](https://github.com/user-attachments/assets/73b20106-a468-45b1-bd47-f333be7e1f8c)

--![vm34](https://github.com/user-attachments/assets/99abe8f6-5a43-46b5-b57b-7c27358536aa)
----------------------------------------------------------------------

## Step 17 -- Configure Health Settings

-   Application health monitoring: Disabled
-   Automatic repairs: Disabled

![vm35](https://github.com/user-attachments/assets/39ffb6e2-1de6-4a02-99b3-3a17fcfae4cb)

------------------------------------------------------------------------

## Step 18 -- Review Advanced Settings

-   Max spreading algorithm
-   No extensions configured

![vm36](https://github.com/user-attachments/assets/e84ff8d9-78c2-4371-99fa-8bf99ce9d7b6)


------------------------------------------------------------------------

## Step 19 -- Review + Create

-   Validation passed
-   Clicked Create

![vm37](https://github.com/user-attachments/assets/31b41300-5aa5-4524-96e7-500417425d4e)
![vm38](https://github.com/user-attachments/assets/821951c7-2bb9-4cf2-88c9-3128a0150527)



------------------------------------------------------------------------

## Step 20 -- Deployment Completed

-   Deployment succeeded
-   Navigated to resource

![vm39](https://github.com/user-attachments/assets/5d2ae076-1460-4d96-9cf8-2aa97d82ab4c)

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

