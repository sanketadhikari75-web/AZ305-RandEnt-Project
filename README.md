# AZ-305 Project
## Automating Workloads using ARM Templates

### Project Overview

Rand Enterprises wanted to deploy infrastructure using ARM Templates.

The solution provisions:

- Virtual Network
- Subnet
- Virtual Machine (Standard_B1s)
- Storage Account (StorageV2)
- Private Endpoint
- Private DNS Zone

### Objective

The Storage Account must not be accessible through the public internet.

Communication between the VM and Storage Account occurs through Azure's internal network using Private Endpoint.

### Architecture

![Architecture](Architecture-Diagram.png)

### Resources Used

| Resource | SKU |
|-----------|--------|
| VM | Standard_B1s |
| OS Disk | Standard_LRS |
| Storage Account | StorageV2 |
| Storage Replication | Standard_LRS |
| Network | VNet + Subnet |
| Connectivity | Private Endpoint |

### Security

- Public Storage Access Disabled
- Private Endpoint Enabled
- Private DNS Zone Configured

### Deployment

The infrastructure is deployed using ARM Template.

### ARM Template

azuredeploy.json
